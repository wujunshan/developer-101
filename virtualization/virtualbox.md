# Oracle VirtualBox 新手入门

### 介绍

[Oracle VirtualBox][virtualbox]  是一款开源虚拟机软件。由德国 Innotek 公司开发，Sun Microsystems 公司出品。使用Qt编写，在 Sun 被 Oracle 收购后正式更名成 Oracle VM VirtualBox。采用 GPL 协议开源



### 安装

**Ubuntu**

本例以Ubuntu 16.04为例，其他 Linux 版本 请参照[VirtualBox 镜像使用帮助][tsinghua]

	wget -q https://www.virtualbox.org/download/oracle_vbox_2016.asc -O- | \
	      sudo apt-key add -
	
	echo  "deb https://mirrors.tuna.tsinghua.edu.cn/virtualbox/apt/ xenial contrib" | \
	      sudo tee -a /etc/apt/sources.list.d/virtualbox.list
	
	sudo apt-get update
	sudo apt-get install virtualbox-5.1
	
安装 [VirtualBox Extension Pack][extension] 获得更多功能支持(USB、RDP、PXE)。

	VBoxManage extpack install --replace \
      /tmp/Oracle_VM_VirtualBox_Extension_Pack-5.1.8-111374.vbox-extpack



**Mac**


	brew cask install virtualbox virtualbox-extension-pack

	
[virtualbox]: https://www.virtualbox.org/
[tsinghua]: https://mirrors.tuna.tsinghua.edu.cn/help/virtualbox/