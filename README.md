# YES Lab ROS Task

## 安装步骤

1. 安装 VMware Workstation Pro 17.6.4（Personal Use 免费版）
2. 新建虚拟机（内存4G、CPU 2核、硬盘30G、3D加速128MB）
3. 挂载 Ubuntu 20.04.6 桌面版 ISO，完成系统安装
4. 换清华系统源
5. 添加 ROS 清华源 + 密钥
6. 安装 ros-noetic-desktop-full
7. 配置环境变量

## 遇到的问题及解决办法

### 问题1：VirtualBox 反复报 E_FAIL/hardening 错误
- 解决：弃用 VirtualBox，改用 VMware Workstation Pro 17.6.4

### 问题2：直接安装 ROS 提示"无法定位软件包"
- 原因：跳过了添加 ROS 源和密钥的步骤
- 解决：补加 ROS 清华源 + 导入公钥，再执行 apt update 后安装

### 问题3：sudo apt update 报 NO_PUBKEY 错误
- 解决：执行 sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654

### 问题4：小海龟启动但方向键控制不动
- 原因：键盘焦点没在控制终端上
- 解决：点击控制终端激活 + Ctrl+G 捕获 VMware 键盘

## 运行截图与录屏


