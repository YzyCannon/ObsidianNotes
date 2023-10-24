### 1. 修改屏幕朝向:
```
hdc shell mount -o remount,rw /

hdc shell chmod 777 /system/etc/window/resources/display_manager_config.xml

hdc shell

export PATH="$PATH:/system/busybox"

vi /system/etc/window/resources/display_manager_config.xml

reboot
```
### 2. 屏幕常亮
```
hdc shell power-shell setmode 602
```
### 3.busybox安装指南
#### 获取读写权限
```
hdc smode 

hdc shell mount -oremount,rw /
```
#### 安装busybox
```
hdc file send busybox /system/bin/busybox 

hdc shell chmod a+x /system/bin/busybox 

hdc shell mkdir /system/busybox 

hdc shell busybox --install -s /system/busybox
```
#### 使用busybox环境
```
hdc shell 
export PATH="$PATH:/system/busybox"
```
### 4.刷机
```
hdc shell reboot loader
```
### 截图
```
hdc shell "snapshot_display -f /data/0.jpeg"

hdc file recv /data/0.jpeg
```