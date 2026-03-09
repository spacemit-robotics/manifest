# SpacemiT Robot SDK Manifest

本仓库为 SpacemiT Robot SDK 的 [repo](https://gerrit.googlesource.com/git-repo) manifest 配置，用于统一管理多仓库代码的拉取与同步。

## 前置要求

- Ubuntu/Debian 系统
- repo

```bash

sudo apt update
sudo apt install repo
```

## 初始化工作空间

当前这份 manifest 可同时用于 GitHub 与 Gitee，仓库来源由 `repo init -u` 指向的 manifest 地址决定。

```bash
mkdir spacemit_robot
cd spacemit_robot


# 方式一：使用GitHub
repo init -u https://github.com/spacemit-robotics/manifest.git -b main -m default.xml
repo sync -j4
repo start robot-dev --all

# 方式二：使用Gitee：

repo init -u https://gitee.com/spacemit-robotics/manifest.git -b main -m default.xml
repo sync -j4
repo start robot-dev --all
```


## 项目结构

```bash
spacemit_robot
.
├── application
│   └── native
│       └── omni_agent
├── build
├── components
│   ├── agent_tools
│   │   └── mcp
│   ├── model_zoo
│   │   ├── asr
│   │   ├── llm
│   │   ├── tts
│   │   ├── vad
│   │   └── vision
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