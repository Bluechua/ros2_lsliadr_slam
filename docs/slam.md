# 三、SLAM建图实操
## toolbox建图
### SLAM Toolbox实时建图完整流程
SLAM Toolbox是ROS2官方推荐的轻量化建图工具，适配M10P网口激光雷达，支持实时构图、动态避障。

#### 1. 前置准备
雷达驱动必须正常启动，确认 `/scan` 话题持续输出点云数据：
```bash
# 新开终端查看雷达话题
ros2 topic echo /scan

# 一键启动雷达+实时建图
ros2 launch lslidar_driver slam_toolbox_m10p.launch.py

rviz2 -d install/lslidar_driver/share/lslidar_driver/rviz/slam.rviz

ros2 launch lslidar_driver gmapping_m10p.launch.py

# 保存地图到当前终端目录，地图命名room_map
ros2 run nav2_map_server map_saver_cli -f room_map