# Games101 作业工程

## 1. 概要

本工程使用 cmake 搭建，各作业的文档统一放置在 doc 目录下

## 1. 如何构建

### 1.1 构建所需要的软件

- cmake
- vcpkg
    - vcpkg 的根目录应当设置为 `VCPKG_ROOT` 的环境变量

### 1.2 构建参数

工程文件中的 .vscode 目录下存有两个配置参数，即
```json
"cmake.configureArgs": [
        "-DCMAKE_TOOLCHAIN_FILE=$ENV{VCPKG_ROOT}/scripts/buildsystems/vcpkg.cmake",
        "-DVCPKG_TARGET_TRIPLET=x64-windows"
    ]
```
如果你不使用 vscode 作为编辑器，那么就应当在其他编辑器配置文件中，或者直接将上述二参数作为命令行参数传入 cmake 的配置过程。其中，`VCPKG_TARGET_TRIPLET`视当前的编译环境而定，具体可参见 vcpkg 的[三元组](https://learn.microsoft.com/en-us/vcpkg/users/triplets)说明。