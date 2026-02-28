# SpacemiT Robot SDK Manifest

本仓库为 SpacemiT Robot SDK 的 [repo](https://gerrit.googlesource.com/git-repo) manifest 配置，用于统一管理多仓库代码的拉取与同步。

## 前置要求

- Ubuntu/Debian 系统
- Git 2.9+

```bash
# 安装构建工具及 repo
sudo apt install -y \
    build-essential \
    cmake \
    pkg-config \
    git \
    repo \
    curl \
    wget
```

## 初始化工作空间

```bash
mkdir spacemit_robot
cd spacemit_robot
repo init -u https://github.com/spacemit-robotics/manifest.git -b main -m default.xml
repo sync -j4
repo start robot-dev --all
```

使用 SSH 时：

```bash
repo init -u git@github.com:spacemit-robotics/manifest.git -b main -m default.xml
```

## 项目结构

```bash
spacemit_robot
.
├── build
├── components
│   ├── multimedia
│   │   └── audio
│   └── peripherals
│       ├── imu
│       ├── key
│       ├── lidar
│       ├── light_sensor
│       ├── misc_io
│       ├── motor
│       └── nfc
├── scripts
└── target
```