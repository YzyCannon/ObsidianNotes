### 无法远程连接
首先检查检查ip是否正确；
如果不是ip的问题，直接输入以下命令再连接
```
sudo apt-get update 
sudo apt-get install xrdp 
sudo apt-get install vnc4server 
sudo apt-get install xubuntu-desktop 
sudo service xrdp restart
```
### 启动xrdp，通过远程连接访问Ubuntu桌面
```
sudo systemctl restart xrdp
```
### 快速打开VSCode
```
code .
```

## 由于没有公钥，无法验证下列签名： NO_PUBKEY 76F1A20FF987672F
[由于没有公钥，无法验证下列签名： NO_PUBKEY 76F1A20FF987672F_由于没有公钥，无法验证下列签名： no_pubkey 2ea8f35793d8809a-CSDN博客](https://blog.csdn.net/weixin_44172434/article/details/89160720)

## Linux(Ubuntu系统)安装yum及源的更新(详细操作+文字描述！！！)
[Linux(Ubuntu系统)安装yum及源的更新(详细操作+文字描述！！！)_ubuntu更新yum源_小石y的博客-CSDN博客](https://blog.csdn.net/qq_45261963/article/details/117520995)

##  将CentOS/ubuntu的目录添加到windows的网络位置/将centOS目录影射为windows网络驱动器
[将CentOS/ubuntu的目录添加到windows的网络位置/将centOS目录影射为windows网络驱动器_陈 洪 伟的博客-CSDN博客](https://blog.csdn.net/u013171226/article/details/119807726#:~:text=%E5%9C%A8windows,%E5%86%99public%E3%80%82)
## Windows无法访问samba服务器解决办法
[Windows无法访问samba服务器解决办法_samba无法访问-CSDN博客](https://blog.csdn.net/weixin_43890955/article/details/102579960)

# ubuntu20.04更换清华源
[ubuntu20.04更换清华源_PisaYu的博客-CSDN博客](https://blog.csdn.net/qq_42620328/article/details/116313697)
### 清华源 [ubuntu | 镜像站使用帮助 | 清华大学开源软件镜像站 | Tsinghua Open Source Mirror](https://mirrors.tuna.tsinghua.edu.cn/help/ubuntu/)

## linux与windows文件共享
[linux与windows文件共享_windows访问linux共享文件夹-CSDN博客](https://blog.csdn.net/L1506812723/article/details/130527985)


```
ln -s apt_pkg.cpython-38m-x86_64-linux-gnu.so apt_pkg.so 
ln -s apt_pkg.cpython-310-x86_64-linux-gnu.so apt_pkg.so 
apt_pkg.cpython-310-x86_64-linux-gnu.so
```

```
cp apt_pkg.cpython-310-x86_64-linux-gnu.so apt_pkg.cpython-38m-x86_64-linux-gnu.so 
```

### ubuntu22.04 默认python3.10
#### 切换python3.8
[How to Install Python 3.8 on Ubuntu 22.04 LTS_51CTO博客_ubuntu安装python3.8](https://blog.51cto.com/ganzy/5636414)
#### ModuleNotFoundError: No module named 'distutils.cmd'
```
 sudo apt-get install python3.8-distutils
```

#### ModuleNotFoundError: No module named 'apt_pkg'
[解决安装Python版本出现No module named 'apt_pkg'问题 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/547673946)

#### ERROR: Could not find a version that satisfies the requirement PyYAML (from ohos-build) (from versions: none) ERROR: No matching distribution found for PyYAML
[pip安装包报错Could not find a version that satisfies the requirement pymysql (from versions: none) - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/361790784)
pip install --user build/lite -i http://pypi.douban.com/simple/ --trusted-host pypi.douban.com


