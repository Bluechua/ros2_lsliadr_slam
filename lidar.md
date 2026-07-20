# 一、雷达硬件准备
## 硬件接线
M10P激光雷达使用网线直连Ubuntu电脑。

## Ubuntu网口IP配置
如果更换设备需要配置电脑IP，有线网口IPv4设为同一网段：
1. 点击 Edit Connections，双击对应有线网卡
2. IPv4 Settings 中 Method 改为 Manual
3. Address 设置：192.168.1.102，子网掩码24
4. 点击 Routes，勾选 Use this connection only for resources on its network

雷达出厂固定IP：192.168.1.200

## 串口/网口查看命令
```bash
# 查看以太网设备
ip a
# 测试雷达连通性
ping 192.168.1.200
