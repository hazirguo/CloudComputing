VirtaulBox 如果虚拟机的网络设置为 NAT 模式，这样虚拟机的网络对主机是不可见的，如果此时主机想通过网络访问主机该怎么做呢？

下面给出两种方法：

* 将网络设置为桥接（Bridge)模式，这样虚拟机分配了一个与主机在同一个网络的 IP
* 通过端口映射，这种方法和外网想访问局域网内某台机器的原理是一样的。

下面介绍怎样进行端口映射，完成在主机下通过 Putty 的 ssh 到虚拟机上：

* 通过 GUI 方式设置端口映射：
    * 在虚拟机下的菜单栏找到**设置** --> **网络** --> **端口转发** （注意检查网络连接是否是 NAT 模式）
    
    ![](http://i.imgur.com/XzibMBG.png)
    
    * 可以添加转发规则，每栏的含义是：
        * 名称：为规则取个名称，可以任取
        * 协议：选择是 TCP/UDP 协议
        * 主机IP：可以不填
        * 主机端口：填一个不与在用的端口冲突的端口即可
        * 子系统IP：虚拟机IP，如果只有一个虚拟机在用，可以不填
        * 子系统端口：你需要转发的端口号
    
    ![](http://i.imgur.com/bONROzQ.png)
    
    * 如果我想在主机通过 ssh 连接到虚拟机，那么就即为 22 端口号映射一个主机端口号，这里我设置为 2222
* 打开 Putty 等类似软件，填上本机的 IP 以及端口号（127.0.0.1:2222），这时 VirtualBox 会为你转发到虚拟机的 22 端口，即完成 ssh 连接虚拟机
* 注意：如果出现 Putty 不能连接上，有可能是虚拟机没安装 ssh-server（默认只安装了 ssh 的客户端，而没有安装 ssh 的服务端），在 Ubuntu 下可以通过命令 `apt-get install openssh-server` 来完成安装。
