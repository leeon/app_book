###Vagrant?

对于多数开发者而言，Linux 是最佳的编程环境。现实情况常常是，我们希望程序运行在 Linux 环境中，而我们在自己习惯的 OS 中编写程序。例如在 Mac 或者 Windows 中编写程序常常遇到的问题是：开发环境难以管理，想想重装系统后的痛苦；其次是经典的『在我这里就可以运行』的 bug。

在过去，有些开发者会在本地搭建一套虚拟机，然后 ssh 到虚拟机环境中，去编译和运行程序。虚拟机的问题是比较臃肿，配置麻烦，而已维护起来也不够灵活。

有了 Vagrant 之后，我们几乎可以在三条命令之内就完成了过去这些繁琐的事情了。Vagrant 中包含了几个核心的概念：

#####Vagrantfile
没错，整个环境我们就只需要这一个配置文件。

#####Provider
Provider 就是各种 VN 包括 VirtualBox，Vmware 甚至目前流行的 Docker，这些能为我们提供虚拟化的工具。

#####Box
Box就是我们的所需要的一个OS环境，[www.vagrantbox.es](http://www.vagrantbox.es/)上面提供了很多封装好的 Box. 这些 Box 都可以直接使用。例如，你可能需要一个配置好的 LAMP 环境的 Box，都可以直接在上面寻找，下载到本地后，就可以直接使用。你可以使用最基础的 Ubuntu 系统原始 Box，自己配置所需的软件环境，然后通过 `vagrant pakcage` 命令打包后，就可以作为备份或者分发给项目组里的其他成员去使用。


#####Provisioner
Provisioners可以是你在 Vagrantfile 中配置好所需的软件包，在虚拟机起动的时候，这些软件会被自动安装好。

###Usage

###Config