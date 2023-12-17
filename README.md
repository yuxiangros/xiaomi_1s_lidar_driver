1.雷达接线
红色:3.3V
黑色:GND
白色:GND
棕色:RXD
黄色:TXD
橘黄:5V
参考doc/wire_connection.png

2.代码修改
/dev/ttyUSB0 根据自己的实际需求进行修改
参考doc/code_modified.png

3.编译
catkin_make_isolated -j4

4.运行
4.1 sudo chmod 777 /dev/ttyUSB0 
4.2 source devel/setup.bash
4.3 rosrun xv_11_laser_driver neato_laser_publisher _port:=/dev/ttyUSB0 _firmware_version:=2

5.rviz 设置
Fixed frame 设置为neato_laser
LaserScan Topic 设置为 /scan
参考doc/rviz_settings.png