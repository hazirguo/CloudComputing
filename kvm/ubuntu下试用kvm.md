### 准备工作

* 查看CPU是否支持虚拟化：`egrep '(vmx|svm)' /proc/cpuinfo `
* 在 BIOS 开启 CPU 虚拟化功能

### Ubuntu 下安装 KVM

使用命令安装：`sudo apt get install kvm`

### 创建虚拟镜像

```
kvm-img create xxx.img 2G
```

创建了一个 2G 大小的虚拟镜像。

### 安装虚拟机系统

我们下载了一个 32 位 windows xp 操作系统，使用下面命令安装该虚拟机系统：

```
kvm -drive file=xxx.img -cdrom /path/to/boot-media.iso -boot d -m 512
```

### 使用虚拟机

安装完成之后，即可开启该虚拟机：

```
kvm -m 1024 -drive file=xxx.img
```

