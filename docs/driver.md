# ROS2雷达驱动部署
## 编译安装
### 1. 进入ROS2工作空间src目录
所有源码包都放在src文件夹下（官方开源驱动包在百度网盘ROS2_SDK压缩包内，下载解压后放入该目录）。

### 2. 雷达与ROS2驱动连接说明
本次使用设备型号：lslidar_m10p_net 网口激光雷达。

## 全套终端执行命令
```bash
# 安装雷达运行依赖库
sudo apt-get install libpcap-dev
# 切换至ROS2工作空间src目录
cd ~/ros2_ws/src
# 编译完成后，启动雷达节点
ros2 launch lslidar_driver lslidar_m10p_launch.py