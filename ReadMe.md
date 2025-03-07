# [libwsk](https://github.com/mirokaku/libwsk)

[![Actions Status](https://github.com/MiroKaku/libwsk/workflows/CodeQL/badge.svg)](https://github.com/MiroKaku/libwsk/actions)
[![LICENSE](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/MiroKaku/libwsk/blob/master/LICENSE)
![Windows](https://img.shields.io/badge/Windows-10%20RS2+-orange.svg)
![Visual Studio](https://img.shields.io/badge/Visual%20Studio-2019-purple.svg)

* [简体中文](ReadMe.zh-cn.md)

## About

libwsk is a wrapper for the [WSK (Winsock-Kernel)](https://docs.microsoft.com/en-us/windows-hardware/drivers/network/introduction-to-winsock-kernel) interface. With libwsk, kernel-mode software modules can perform network I/O operations using the same socket programming concepts and interface that are supported by user-mode Winsock2.

## Build and used

IDE：Visual Studio 2019 or higher

1. git clone https://github.com/MiroKaku/libwsk.git
2. Open the `msvc/libwsk.sln` and build it.
3. include `libwsk.lib` to your project. refer `unittest`。

## Supported progress

| BSD sockets   | WSA (Windows Sockets API) | WSK (Windows Sockets Kernel) | State  
| ---           | ---                       | ---                          | :----: 
| -             | WSAStartup                | WSKStartup                   |   √    
| -             | WSACleanup                | WSKCleanup                   |   √    
| socket        | WSASocket                 | WSKSocket                    |   -    
| bind          | -                         | WSKBind                      |   -    
| listen        | -                         | WSKListen                    |   -    
| connect       | WSAConnect                | WSKConnect                   |   -    
| accept        | WSAAccept                 | WSKAccept                    |   -    
| send          | WSASend                   | WSKSend                      |   -    
| recv          | WSARecv                   | WSKRecv                      |   -    
| sendto        | WSASendTo                 | WSKSendTo                    |   -    
| recvfrom      | WSARecvFrom               | WSKRecvFrom                  |   -    
| ...           | ...                       | ...                          |   -    

## Reference

* [wbenny/KSOCKET](https://github.com/wbenny/KSOCKET)
* [microsoft/docs](https://docs.microsoft.com/zh-cn/windows-hardware/drivers/network/introduction-to-winsock-kernel)
