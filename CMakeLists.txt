cmake_minimum_required(VERSION 3.14 FATAL_ERROR)

list(APPEND CMAKE_MODULE_PATH "${CMAKE_CURRENT_SOURCE_DIR}/cmake/")
include(pkg-utils)

pkg_get_version(LDK ${CMAKE_CURRENT_SOURCE_DIR}/include/ldk/internal/version.h VERSION)

project(Ldk VERSION "${VERSION}" LANGUAGES C)

if ("${CMAKE_VS_PLATFORM_NAME}" STREQUAL "x64")
    option(LDK_USE_RAISE_EXCEPTION  "Set to ON to use ldk!RaiseException" ON)
    option(LDK_USE_RTL_RAISE_EXCEPTION  "Set to ON to use ldk!RtlRaiseExceptionn" ON)
else()
    option(LDK_USE_RAISE_EXCEPTION  "Set to ON to use ldk!RaiseException" OFF)
    option(LDK_USE_RTL_RAISE_EXCEPTION  "Set to ON to use ldk!RtlRaiseExceptionn" OFF)
endif()

include(CPM)
CPMAddPackage("gh:ntoskrnl7/FindWDK#master")
list(APPEND CMAKE_MODULE_PATH "${FindWDK_SOURCE_DIR}/cmake")
find_package(WDK REQUIRED)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} /W4 /WX")
set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} /W4 /WX")

file(GLOB SOURCE_FILES ./src/*.c ./src/*/*.c ./src/ntdll/rtl/*.c)

wdk_add_library(Ldk STATIC ${SOURCE_FILES})

target_compile_definitions(Ldk PUBLIC -D_KERNEL32_)
if (LDK_USE_RAISE_EXCEPTION)
    target_compile_definitions(Ldk PUBLIC -D_LDK_DEFINE_RAISE_EXCEPTION)
endif()
if (LDK_USE_RTL_RAISE_EXCEPTION)
    target_compile_definitions(Ldk PUBLIC -D_LDK_DEFINE_RTL_RAISE_EXCEPTION)
    # ntoskrnl.lib(ntoskrnl.exe) : error LNK2005: RtlRaiseException already defined in Ldk.lib(except.obj).
    target_link_options(Ldk PUBLIC "/FORCE:MULTIPLE")
endif()

string( TOLOWER "${CMAKE_VS_PLATFORM_NAME}" PLATFROM_SHORT_NAME )
if( PLATFROM_SHORT_NAME STREQUAL "win32" )
    set(PLATFROM_SHORT_NAME "x86")
endif()

set_target_properties(Ldk PROPERTIES ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/lib/${PLATFROM_SHORT_NAME})

target_include_directories(Ldk PUBLIC $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>)

#
# Generate Debug Info
#
target_compile_options(Ldk PUBLIC "$<$<CONFIG:Release>:/Zi>")
target_link_options(Ldk PUBLIC "$<$<CONFIG:Release>:/DEBUG>")

#
# set library output path (release only)
#
string(TOLOWER "${CMAKE_VS_PLATFORM_NAME}" PLATFROM_SHORT_NAME)
if(PLATFROM_SHORT_NAME STREQUAL "win32")
    set(PLATFROM_SHORT_NAME "x86")
endif()
set_target_properties(Ldk PROPERTIES ARCHIVE_OUTPUT_DIRECTORY_RELEASE ${CMAKE_CURRENT_SOURCE_DIR}/lib/${PLATFROM_SHORT_NAME})