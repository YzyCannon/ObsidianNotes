# Stream流
![[Pasted image 20231018212934.png]]
### 1
![[Pasted image 20231018213023.png]]
### 2
![[Pasted image 20231020153443.png]]
### 3
![[Pasted image 20231020153643.png]]
# 方法引用
![[Pasted image 20231020154128.png]]
#### 1.匿名内部类
![[Pasted image 20231020154337.png]]
#### 2.lambda表达式
![[Pasted image 20231020154406.png]]
#### 3.lambda表达式简化
![[Pasted image 20231020154738.png]]
#### 4.方法引用
![[Pasted image 20231020155509.png]]
### 总结
![[Pasted image 20231020155922.png]]
## 引用静态方法

![[Pasted image 20231021170221.png]]
## 引用成员方法
![[Pasted image 20231021171354.png]]
#### 1.其他类
![[Pasted image 20231021170712.png]]
#### 2.本类
![[Pasted image 20231021170541.png]]
![[Pasted image 20231021172039.png]]
#### 3.父类
![[Pasted image 20231021171721.png]]
## 引用构造方法
![[Pasted image 20231021172303.png]]
![[Pasted image 20231021173723.png]]
![[Pasted image 20231021173750.png]]



## 类名引用成员方法
![[Pasted image 20231021174229.png]]
![[Pasted image 20231021174338.png]]

![[Pasted image 20231021175226.png]]
![[Pasted image 20231021180114.png]]

![[Pasted image 20231021180015.png]]

## 引用数组的构造方法
![[Pasted image 20231021180201.png]]
![[Pasted image 20231021180710.png]]
## 总结
![[Pasted image 20231021180909.png]]
![[Pasted image 20231021180922.png]]


# 异常
##  概述
![[Pasted image 20231022174812.png]]
![[Pasted image 20231022174825.png]]

![[Pasted image 20231022174943.png]]

![[Pasted image 20231022175151.png]]
### 四种情况
![[Pasted image 20231022180201.png]]
![[Pasted image 20231022180354.png]]
## 快捷键
ctrl + alt + t
![[Pasted image 20231022191416.png]]

## Throwable成员方法
![[Pasted image 20231022191840.png]]
## 抛出异常 throws 和 throw
![[Pasted image 20231022192116.png]]
## 总结
![[Pasted image 20231022193207.png]]
![[Pasted image 20231022201632.png]]
## 自定义异常
![[Pasted image 20231022205205.png]]
![[Pasted image 20231022205249.png]]

# File

![[Pasted image 20231022210440.png]]
![[Pasted image 20231022210451.png]]
![[Pasted image 20231022210819.png]]


# IO流
![[Pasted image 20231022211120.png]]
![[Pasted image 20231022211132.png]]
程序（内存，程序运行在内存中）在读写数据
![[Pasted image 20231022211727.png]]
## FileOutputStream
#### 概述
![[Pasted image 20231022212655.png]]
![[Pasted image 20231022212802.png]]
#### 细节
![[Pasted image 20231022214718.png]]
![[Pasted image 20231022214752.png]]
#### 总结
![[Pasted image 20231022215055.png]]


## FileInputStream
#### 概述
![[Pasted image 20231022215417.png]]

![[Pasted image 20231022215326.png]]
#### 循环读取
![[Pasted image 20231022215902.png]]
![[Pasted image 20231022215756.png]]
#### 一次读取多个
![[Pasted image 20231022220325.png]]
![[Pasted image 20231022220959.png]]

### 拷贝
小文件，速度慢
![[Pasted image 20231022220051.png]]
速度快
![[Pasted image 20231022221531.png]]
## 异常处理
![[Pasted image 20231022222103.png]]
### 简化代码设计思想
![[Pasted image 20231022222313.png]]
![[Pasted image 20231022222454.png]]
# 字符流
![[Pasted image 20231023202906.png]]
### FileReader
![[Pasted image 20231023203111.png]]
### Filewriter
![[Pasted image 20231023203203.png]]
# 多线程
## 概述
![[Pasted image 20231023204717.png]]
![[Pasted image 20231023205105.png]]
### 线程和进程的区别
[进程和线程的区别(超详细) - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/520460326
**进程和线程都是一个时间段的描述，是CPU工作时间段的描述，不过是颗粒大小不同。**

**根本区别**：进程是资源分配的最小单位，线程是CPU调度的最小单位
**资源开销**：每个进程都有独立的代码和数据空间（程序上下文），程序之间的切换会有较大的开销；线程可以看做轻量级的进程，同一类线程共享代码和数据空间，每个线程都有自己独立的运行栈和程序计数器（PC），线程之间切换的开销小。
**内存分配**：同一进程的线程共享本进程的地址空间和资源，而进程之间的地址空间和资源是相互独立的
**影响关系**：一个进程崩溃后，在保护模式下不会对其他进程产生影响，但是一个线程崩溃整个进程都死掉。所以多进程要比多线程健壮。
**执行过程**：每个独立的进程有程序运行的入口、顺序执行序列和程序出口。但是线程不能独立执行，必须依存在应用程序中，由应用程序提供多个线程执行控制，两者均可并发执行.
## 实现方式
### 三种方式
![[Pasted image 20231023210916.png]]
### entends Thread
![[Pasted image 20231023205857.png]]
### implements Runnable
![[Pasted image 20231023210447.png]]
### implements Callable<>
![[Pasted image 20231023210842.png]]
## 常用成员方法
![[Pasted image 20231023211302.png]]
#### Java中采用*抢占式调度*-*随机*
![[Pasted image 20231023211417.png]]
#### 守护线程
主线程执行结束，守护线程随之结束
![[Pasted image 20231023212023.png]]  
#### 出让线程（结果更均匀，非绝对）
![[Pasted image 20231023212359.png]]
#### 插入线程
![[Pasted image 20231023212649.png]]
## 生命周期
![[Pasted image 20231023212857.png]]
在Java虚拟机中真正定义的只有*6种状态*。*没有运行状态*，当线程抢夺的CPU执行权力，虚拟机会将当前线程交给操作系统管理。
![[Pasted image 20231023222054.png]]

## 线程安全问题synchronized

	static
	同步代码块 synchronized

![[Pasted image 20231023214029.png]]
### 同步方法
![[Pasted image 20231023214332.png]]代码 Ctrl+M抽取出方法 
![[Pasted image 20231023215353.png]]
![[Pasted image 20231023215021.png]]
## Lock锁
![[Pasted image 20231023220355.png]]
![[Pasted image 20231023220958.png]]
## 死锁
## 生产者和消费者

![[Pasted image 20231023221556.png]]![[Pasted image 20231023221608.png]]
### 阻塞队列
![[Pasted image 20231023221906.png]]
![[Pasted image 20231023221853.png]]
