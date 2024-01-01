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

hdc shell mount -o remount,rw /
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

### 中控
```
mount -o remount,rw /
ifconfig eth0 hw ether 28:75:D8:19:C9:67
/bin/smarthome.sh
```

cat data/watchdog/timertask_record
sudo update-alternatives --install /usr/bin/python python /usr/bin/python3.8 1   
sudo update-alternatives --install /usr/bin/python3 python3/usr/bin/python3.8 1   

### 查找
```
find ./ -name "libhellonapi.z.so"
```

### 下载文件到本地
```
hdc file recv system/lib/module/libhellonapi.z.so D:/
```

### 上传文件
```
hdc file send libhellonapi.z.so /system/lib/module
```

### 解压
```
`tar -cvf xxx.tar /data` : 仅打包  
`tar -zcvf xxx.tar /data` : 打包后，以gzip方式压缩  
`tar -jcvf xxx.tar /data` : 打包后，以bzip2方式压缩
```
### 解压缩  
```
先进入需要解压缩的文件夹下  
`cd /tmp/data`  
`tar -xvf xxx.tar` : 解包  
`tar -zxvf xxx.tar` : 解压gzip压缩文件  
`tar -jxvf xxx.tar` : 解压bzip2压缩文件  
`tar -zxvf xxx.tar.gz etc/passwd` :只解压部分文件夹
```
### docker
```
docker start 69da46e4d1d3 -启动容器

docker exec -it 69da46e4d1d3 /bin/bash -进入容器
```
### 进入根目录
```
cd root/data/harmony/release_code/2023-04-09/OpenHarmony-v3.2-Release/OpenHarmony

```
### 命令行编译
#### 部件
```
./build.sh --product-name hispark_taurus_standard --build-target partA --ccache
```
#### 产品
```
./build.sh --product-name hispark_taurus_standard --ccache
```

#### 增量编译
```
./build.sh --product-name rk3568 --ccache --build-target=hellonapi --target-cpu arm64 
```

#### 全量编译
```
./build.sh --product-name rk3568 --ccache
```

#### 编译加速
```
### 添加 --disable-package-image参数

- 取消最后所有的image镜像文件压缩成tar包的动作
- tar包位置 out\rk3568\images.tar.gz
```

```
### 添加 --ccache 参数:

- ccache会缓存c/c++编译的编译输出，下一次在编译输入不变的情况下，直接复用缓存的产物。用来缓存编译过的.o文件等
- 执行sudo apt-get install ccache命令安装ccache
- 再在 --ccache后添加export CCACHE_NOHASHDIR=“true” 和 export CCACHE_SLOPPINESS=“include_file_ctime” （设置ccache在做hash的时候不hash路径、不检查文件的change time）
```
```

### 添加 --build-only-gn 参数

- 重新执行Preloader、loader、gn，不进行最后的编译动作

> 编译流程主要分为：preloader->loader->gn->ninja这四个过程,标准系统的编译构建过程请参考https://ost.51cto.com/posts/13594
```


### 推送文件至应用沙箱路径
```
hdc file send ${待推送文件的本地路径} /data/app/el1/bundle/public/com.ohos.example/

hdc file send video3.mp4 /data/app/el1/100/base/com.example.videoplayer/

hdc file send video3.mp4 /data/app/el1/100/database/com.example.videoplayer/

hdc file send kikaInput.hap /system/app/com.example.kikakeyboard

hdc file recv system/app/com.example.kikakeyboard/kikaInput.hap
```
