# ROS2雷达驱动部署
## 编译安装
安装运行命令
### 1. 进入ROS2工作空间src目录
所有源码包都放在src文件夹下（官方有开源的驱动包在百度网盘ROS2_SDK里面）
### 2.驱动雷达与ros2连接
我们的雷达型号是lslidar_m10p_net

```bash
#运行命令
sudo apt-get install libpcap-dev
#进入src工作空间
cd ~/ros2_ws/src
#驱动雷达
ros2 launch lslidar_driver lslidar_m10p_launch.py