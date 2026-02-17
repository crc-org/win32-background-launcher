# win32-background-launcher

Windows helper to run processes in the background without showing a console window.

## Purpose

This tool is used to run the CRC daemon on Windows without displaying a console window. When running `crc daemon` directly on Windows, a console window appears and remains visible.
This helper hides that window by starting the process with the [`CREATE_NO_WINDOW`](https://learn.microsoft.com/en-us/windows/win32/procthread/process-creation-flags#flags) flag.

## Build

To build the helper only Golang is needed, run the following command to build:

```
make
```

## Usage

```
win32-background-launcher.exe <binary> [args...]
```

Example:
```
win32-background-launcher.exe crc.exe daemon
```
