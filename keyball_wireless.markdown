---
layout: default
title: keyball_wireless
has_children: false
parent: Wireless
---
## keyball系列无线键盘详情介绍

## 相关介绍
* 目前支持mx开关和凯华choc v1/v2 矮轴开关(凯华矮轴型号v1:1350, v2:1353) <br/>
<br/>
* pcb可选：
* * 1：全部都是mx开关； 
* * 2：全部都是凯华choc v1/v2 矮轴开关； 
* * 3：主键位mx开关，拇指区凯华choc v1/v2矮轴开关<br/>
* 轨迹球可选：
* * 直径25mm四氟球
* * 直径34mm轨迹球
* * 全矮轴版本，除非特意指定，否则默认都是：直径25mm四氟球
* * 正常轴体版本，除非特意指定，否则默认都是：直径34mm轨迹球
<br/>
* 左右键盘上方c口有开关，开关向内侧为打开电池，向两边为关闭电池
* 键盘内侧中间有两个按钮，为reset按钮，刷固件可以双击这个按钮，进入bootloader进行刷固件
* 下方为主手nice view 画面
* * 1：电池电量(仅供参考)
* * 2：该键盘连接状态
* * 3：wpm
* * 4:蓝牙当前连接设备(支持5个设备切换，图示表明连接设备 1)
* * 5:当前层<br/>
![k2](static/keyball/k2.png){: width="100%" }<br/>
<br/>
## 蓝牙切换
* * 默认键位左手左下角为 蓝牙 切层键，通过该键长按进入 'blue' 层
* * 'blue' 层 1，2，3，4，5键位分别代表5个蓝牙设备信息，按下可以切换到对应设备
* * 6是清除保存的所有蓝牙设备信息，如果总是连接不了电脑，可以把保存的蓝牙设备全清了，电脑上的蓝牙连接也清掉，重新连接
* * 7是清除保存的当前连接的蓝牙设备信息，如果总是连接不上，可以把这个设备的蓝牙记录清除，电脑上的蓝牙连接也清掉，重新连接
* * 8是切换下一个蓝牙设备
* * 9是切换下一个蓝牙设备
![k4](static/keyball/k4.png){: width="100%" }<br/>
![k3](static/keyball/k3.png){: width="100%" }<br/>

## 轨迹球相关
* studio不支持修改除了基础键位以外的键值，可以通过keymap editor或者自己在本地修改提交编译
* 鼠标键：在 .keymap文件里面
* * 鼠标左键：&mkp LCLK
* * 鼠标右键：&mkp RCLK
* * 鼠标中键：&mkp MCLK
* 轨迹球功能层：在 config/boards/shields/keyball61/keyball61_right.overlay
* * 设置的层数是从 0 开始，对应数字和.keymap文件里面层
* * automouse-layer = <4>; 对应：mouse_layer 滚动轨迹球会自动切入到这层
* * scroll-layers = <5>; 对应：scroll_layer 进入这层会切换成鼠标滚轮模式，可以进行左右滚动和上下滚动
* * snipe-layers = <6>; 对应：snipe_layer 进入这层会降低鼠标dpi
* 在config/boards/shields/keyball61/keyball61_right.conf里面进行轨迹球相关选项设置，可自行调整
## [点击进入zmk改键介绍](./zmk keymap editor)
## [点击进入键盘源码页面](https://github.com/Aldexuan/zmk-config-keyball61)

## keyball61:<br/>
![61](static/keyball/k1.png){: width="100%" }<br/>

