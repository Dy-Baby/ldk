# ldk

**L**oad **D**ll into **K**ernel space

[![CMake](https://github.com/ntoskrnl7/ldk/actions/workflows/cmake.yml/badge.svg)](https://github.com/ntoskrnl7/ldk/actions/workflows/cmake.yml)
![GitHub](https://img.shields.io/github/license/ntoskrnl7/ldk)
![GitHub release (latest SemVer)](https://img.shields.io/github/v/release/ntoskrnl7/ldk)
![Windows 7+](https://img.shields.io/badge/Windows-7+-blue?logo=windows&logoColor=white)
![Visual Studio 2017+](https://img.shields.io/badge/Visual%20Studio-2017+-682270?logo=visualstudio&logoColor=682270)
![CMake 3.14+](https://img.shields.io/badge/CMake-3.14+-yellow.svg?logo=cmake&logoColor=white)
![Architecture](https://img.shields.io/badge/CPU-x86%20%2F%20x64%20%2F%20ARM%20%2F%20ARM64-blue.svg?logo=data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIj8+CjxzdmcgZW5hYmxlLWJhY2tncm91bmQ9Im5ldyAwIDAgNTIgNTIiIGlkPSJMYXllcl8xIiB2ZXJzaW9uPSIxLjEiIHZpZXdCb3g9IjAgMCA1MiA1MiIgeG1sOnNwYWNlPSJwcmVzZXJ2ZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIiB4bWxuczp4bGluaz0iaHR0cDovL3d3dy53My5vcmcvMTk5OS94bGluayI+CiAgICA8Zz4KICAgICAgICA8cGF0aCBmaWxsPSJ3aGl0ZSIgZD0iTTQ5LDE5LjV2LTJoLTYuOTk4NDEzMXYtNy40OTU3ODg2SDE0LjQwMTYxMTNsLTQuNDAwMDI0NCw0LjUzMDAyOTN2MjcuNDY5OTcwN0gxNy41VjQ5aDJ2LTYuOTk1Nzg4NmgzVjQ5aDJ2LTYuOTk1Nzg4NmgzICAgVjQ5aDJ2LTYuOTk1Nzg4NmgzVjQ5aDJ2LTYuOTk1Nzg4NmgyLjgxMTU4NDVsNC42OTAwMDI0LTUuNjQwMDE0NlYzNC41SDQ5di0yaC02Ljk5ODQxMzF2LTNINDl2LTJoLTYuOTk4NDEzMXYtM0g0OXYtMmgtNi45OTg0MTMxICAgdi0zSDQ5eiBNMzYuMDAxNTg2OSwzMy41MDQyMTE0YzAsMS42NTAwMjQ0LTEuMzQ5OTc1NiwzLTMsM2gtMTRjLTEuNjU5OTczMSwwLTMtMS4zNDk5NzU2LTMtM3YtMTRjMC0xLjY1OTk3MzEsMS4zNDAwMjY5LTMsMy0zaDE0ICAgYzEuNjUwMDI0NCwwLDMsMS4zNDAwMjY5LDMsM1YzMy41MDQyMTE0eiIgLz4KICAgICAgICA8cmVjdCBzdHlsZT0iZmlsbDp3aGl0ZSIgaGVpZ2h0PSIyIiB3aWR0aD0iNyIgeD0iMyIgeT0iMTcuNSIgLz4KICAgICAgICA8cmVjdCBzdHlsZT0iZmlsbDp3aGl0ZSIgaGVpZ2h0PSIyIiB3aWR0aD0iNyIgeD0iMyIgeT0iMjIuNSIgLz4KICAgICAgICA8cmVjdCBzdHlsZT0iZmlsbDp3aGl0ZSIgaGVpZ2h0PSIyIiB3aWR0aD0iNyIgeD0iMyIgeT0iMjcuNSIgLz4KICAgICAgICA8cmVjdCBzdHlsZT0iZmlsbDp3aGl0ZSIgaGVpZ2h0PSIyIiB3aWR0aD0iNyIgeD0iMyIgeT0iMzIuNSIgLz4KICAgICAgICA8cmVjdCBzdHlsZT0iZmlsbDp3aGl0ZSIgaGVpZ2h0PSI3IiB3aWR0aD0iMiIgeD0iMzIuNSIgeT0iMyIgLz4KICAgICAgICA8cmVjdCBzdHlsZT0iZmlsbDp3aGl0ZSIgaGVpZ2h0PSI3IiB3aWR0aD0iMiIgeD0iMjcuNSIgeT0iMyIgLz4KICAgICAgICA8cmVjdCBzdHlsZT0iZmlsbDp3aGl0ZSIgaGVpZ2h0PSI3IiB3aWR0aD0iMiIgeD0iMjIuNSIgeT0iMyIgLz4KICAgICAgICA8cmVjdCBzdHlsZT0iZmlsbDp3aGl0ZSIgaGVpZ2h0PSI3IiB3aWR0aD0iMiIgeD0iMTcuNSIgeT0iMyIgLz4KICAgIDwvZz4KPC9zdmc+)

## Overview

- ??? ??????????????? ????????? ?????? Dll??? Kernel ????????? ???????????? ?????? ?????????????????? Dll??? ????????? ?????? ????????? ??? ????????? ???????????????.
- Kernel32.dll??? Ntdll.dll??? ???????????? ?????? ????????? ??? ?????? ????????? ?????? ????????? ????????? ?????? ????????????????????????.

## Requirements

- Windows 7 ??????
- Visual Studio 2017

## Test Environments

- Windows 10
- Visual Studio 2017

## Contents

- [ldk](#ldk)
  - [Overview](#overview)
  - [Requirements](#requirements)
  - [Test Environments](#test-environments)
  - [Contents](#contents)
  - [Caution](#caution)
  - [Build](#build)
  - [Test](#test)
  - [Usage](#usage)
    - [CMake](#cmake)
      - [CMakeLists.txt](#cmakeliststxt)
    - [main.c](#mainc)
  - [TODO](#todo)

## Caution

??? ??????????????? **?????? ????????????** ???????????????.

1. ***TEB??? PEB??? ???????????? ????????? ?????? ????????? ???????????? ????????????***
2. ***Dll Load??? ?????? ?????????????????? ?????? ????????? ?????? ??? ??????????????? ????????????.***

## Build

Visual Studio ??????????????? ??? ?????????????????? ???????????? ??????????????? ????????????.

***CMake ??????????????? ??? ?????????????????? ?????????????????? [CMake](#cmake) ????????? ??????????????? ????????????.***

1. ?????? ????????? ???????????? ?????????????????? ??????????????? ????????????.

    - Visual Studio ??????
      - {??? ?????????}/msvc/ldk.sln ?????? {??? ?????????}/msvc/ldk.vcxproj??? ????????? ????????? ????????? ????????????.

    - CMake ??????

        ```Batch
        git clone https://github.com/ntoskrnl7/ldk
        cd ldk
        mkdir build && cd build
        cmake .. -DWDK_WINVER=0x0602
        cmake --build . --config Release
        ```

2. ????????? ?????????????????? ?????? ????????? ???????????? ???????????? ??????????????? ??????????????? ????????????.

    1. **{??? ?????????}/include**??? '**[?????? ?????? ????????????](https://docs.microsoft.com/cpp/build/reference/i-additional-include-directories#to-set-this-compiler-option-in-the-visual-studio-development-environment
    )** ??????'??? ??????.
    2. **Ldk.lib**??? '**[?????? ?????????](https://docs.microsoft.com/cpp/build/reference/dot-lib-files-as-linker-input?view=msvc-170#to-add-lib-files-as-linker-input-in-the-development-environment)** ??????'??? ??????.
    3. **{??? ?????????}/lib/\$(PlatformShortName)/\$(Configuration)**??? '**[?????? ??????????????? ????????????](https://docs.microsoft.com/cpp/build/reference/libpath-additional-libpath?view=msvc-170#to-set-this-linker-option-in-the-visual-studio-development-environment)** ??????'??? ??????

## Test

1. ?????? ????????? ???????????? ??????????????? ??? ????????? ????????? ??????????????? ????????????.

    ```Batch
    git clone https://github.com/ntoskrnl7/ldk
    cd ldk/test
    mkdir build && cd build
    cmake .. -DWDK_WINVER=0x0602
    cmake --build .
    ```

2. build/Debug/LdkTest.sys??? ?????? ??? ??????????????? ????????????.
3. ??????????????? ?????? ??? ???????????? ????????? ??????????????? ????????????.

## Usage

CMake??? ?????????????????? ???????????????.

### CMake

CMake??? ?????????????????? ????????? ?????? CMakeLists.txt??? ???????????? ????????????.

#### CMakeLists.txt

```CMake
cmake_minimum_required(VERSION 3.14 FATAL_ERROR)

# create project
project(MyProject)

# add dependencies
include(cmake/CPM.cmake)
CPMAddPackage("gh:ntoskrnl7/ldk@0.7.5")

# add dependencies
CPMAddPackage("gh:ntoskrnl7/FindWDK#master")

# use FindWDK
CPMAddPackage("gh:ntoskrnl7/FindWDK#master")
list(APPEND CMAKE_MODULE_PATH "${FindWDK_SOURCE_DIR}/cmake")
find_package(WDK REQUIRED)

# add driver
wdk_add_driver(TestDrv CUSTOM_ENTRY_POINT "LdkDriverEntry" main.c)

# link dependencies
target_link_libraries(TestDrv Ldk)
```

### main.c

Condition Variable??? ???????????? ????????? ?????? ???????????????.

- ????????? ?????? ???????????? LdkDriverEntry??? ??????????????? LdkInitialize??? LdkTerminate??? ????????? ????????? ????????????. **(??????)**

    ```CMake
    wdk_add_driver(TestDrv CUSTOM_ENTRY_POINT "LdkDriverEntry" main.c)
    ```

- ?????? ????????? ?????? ???????????? ???????????? ???????????? ??????????????? ????????? ?????? LdkInitialize ????????? ????????? ??????????????????, ???????????? ????????? ????????? LdkTerminate ????????? ????????? ?????????????????????.

    ```CMake
    wdk_add_driver(TestDrv main.c)
    ```

????????? LdkDriverEntry??? ??????????????? ????????? ??????????????? ?????? ???????????????.

```C
#include <Ldk/Windows.h>

DRIVER_INITIALIZE DriverEntry;
DRIVER_UNLOAD DriverUnload;

typedef struct _COND_TEST_THREAD_PARAM {
    PCSTR name;
    BOOL ready;
    LONG processed;
    CONDITION_VARIABLE cv;
    CRITICAL_SECTION cs;
} COND_TEST_THREAD_PARAM, *PCOND_TEST_THREAD_PARAM;

DWORD
WINAPI
CondTestThreadProc (
    LPVOID lpThreadParameter
    )
{
    PCOND_TEST_THREAD_PARAM param = (PCOND_TEST_THREAD_PARAM)lpThreadParameter;

    PAGED_CODE();

    DbgPrint("%s - %d - start\n", param->name, GetCurrentThreadId());

    EnterCriticalSection(&param->cs);
    while (!param->ready) {
        SleepConditionVariableCS(&param->cv, &param->cs, INFINITE);
    }

    DbgPrint("%s - %d - processed (%d)\n", param->name, GetCurrentThreadId(), InterlockedIncrement(&param->processed));

    LeaveCriticalSection(&param->cs);

    DbgPrint("%s - %d - end\n", param->name, GetCurrentThreadId());

    WakeConditionVariable(&param->cv);
    return 0;
}

NTSTATUS
DriverEntry (
    _In_ PDRIVER_OBJECT DriverObject,
    _In_ PUNICODE_STRING RegistryPath
    )
{
    PAGED_CODE();
    UNREFERENCED_PARAMETER(RegistryPath);

    COND_TEST_THREAD_PARAM param;
    param.name = "Test";
    param.ready = FALSE;
    param.processed = 0;
    InitializeCriticalSection(&param.cs);
    InitializeConditionVariable(&param.cv);
    HANDLE threads[5];
    for (int i = 0; i < 5; ++i) {
        threads[i] = CreateThread(NULL, 0, CondTestThreadProc, &param, 0, NULL);
    }

    EnterCriticalSection(&param.cs);
    param.ready = TRUE;
    LeaveCriticalSection(&param.cs);
    WakeAllConditionVariable(&param.cv);

    EnterCriticalSection(&param.cs);
    while (param.processed < 5) {
        SleepConditionVariableCS(&param.cv, &param.cs, INFINITE);
    }
    WakeAllConditionVariable(&param.cv);
    LeaveCriticalSection(&param.cs);

    WaitForMultipleObjects(5, threads, TRUE, INFINITE);
    DeleteCriticalSection(&param.cs);

    for (int i = 0; i < 5; ++i) {
        if (threads[i]) {
            CloseHandle(threads[i]);
        }
    }

    DriverObject->DriverUnload = DriverUnload;
    return STATUS_SUCCESS;
}

VOID
DriverUnload (
    _In_ PDRIVER_OBJECT driverObject
    )
{
    PAGED_CODE();
    UNREFERENCED_PARAMETER(driverObject);
}
```

## TODO

 ?????? Dll??? ???????????? ?????????????????? API??? ???????????? ???????????? ????????? ????????? Dll ????????? ????????? ??? ????????????.

- [ ] ?????? ????????? ????????? ReactOS ????????? ?????? ??????????????????, ?????? ?????? ?????????????????????.
- [ ] ?????????
- [ ] ??????
