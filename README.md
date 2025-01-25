# Liteboty Stream

Liteboty Stream 是一个基于 Redis 的视频流监控系统，可以订阅并显示来自 Redis 频道的视频流数据。

## 功能特点

- 支持多视频流同时显示
- 提供图形界面和命令行两种使用方式
- 支持多种图像解码格式（RGB、L等）
- 窗口大小自适应调整
- 支持窗口层叠和平铺排列

## 安装

使用 pip 安装：
```bash
pip install liteboty-stream
```

## 使用方法

### 图形界面模式

启动图形界面：
```bash
liteboty-stream ui
```


在图形界面中：
1. 点击"新建视频流"按钮或使用快捷键 `Ctrl+N`
2. 在弹出的对话框中填写：
   - Redis 地址（例如：10.8.2.2:6379）
   - 订阅频道（例如：/video/raw）
   - 解码格式（默认：RGB）
3. 点击"确定"添加新的视频流窗口

### 命令行模式

直接启动单个视频流窗口：

```bash
liteboty-stream run --broker 10.8.2.2:6379 --channel /video/raw --decode RGB
```


参数说明：
- `--broker`：Redis 服务器地址（必填）
- `--channel`：Redis 订阅频道（必填）
- `--decode`：图像解码格式，默认为 RGB

## 快捷键

- `Ctrl+N`：新建视频流
- `Ctrl+Q`：退出程序

## 系统要求

- Python 3.10 或更高版本
- Redis 服务器
- 支持的操作系统：Windows、Linux、macOS

## 依赖项

- PySide6
- Redis
- Pillow
- Click
- Liteboty

## 许可证

本项目基于 MIT 许可证开源。

## 问题反馈

如果您在使用过程中遇到任何问题，请访问我们的 [GitHub 仓库](https://github.com/yejue/liteboty) 提交 Issue。