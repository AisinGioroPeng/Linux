# Ubuntu安装方法和环境配置



#### **安装方法**

+ /boot:系统区，但是随着ubuntu版本更新过快，建议配置1024M或2048M左右
+ /swap: 一般建议虚拟机与分配给虚拟机的内存大小保持一致，比如虚拟机内存4G，那么/swap区给4096M
+ 具体安装方法参考CSDN：<https://blog.csdn.net/u012808186/article/details/119142280?spm=1001.2014.3001.5506>



#### **VMware全屏显示虚拟机**

1. 安装[VMware](https://so.csdn.net/so/search?q=VMware&spm=1001.2101.3001.7020) tools:	虚拟机 -- 重新安装VMWare Tools(T)...
2. 查看 -- 自适应客户机



#### ubuntu设置开机自动启动小键盘

+ 方法1（使用有效）：
  1. 编辑虚拟机设置(虚拟机设置)
  2. 选项
  3. 增强型键盘(K):在可用时使用(推荐)

+ 方法2（暂未使用过）：

  1. ```bash
     sudo apt-get install numlockx
     ```

  2. ```bas
     sudo gedit /usr/share/lightdm/lightdm.conf.d/50-unity-greeter.conf
     ```

  3. ```cpp
     在最后添加：greeter-setup-script=/usr/bin/numlockx on
     ```

  4. ```
     具体操作参考<https://zhuanlan.zhihu.com/p/168066986>
     ```



#### ubuntu安装搜狗输入法的方法

+ 具体安装方法参考<https://shurufa.sogou.com/linux/guide>（一定要看到底下，不要忘记安装搜狗输入法依赖库）



**ubuntu安装QtCreator方法：**

+ 具体安装方法参考https://blog.csdn.net/qq_16377055/article/details/117958239



#### Qt运行时报错1

+ Qt Warning: Ignoring XDG_SESSION_TYPE=wayland on Gnome. Use QT_QPA_PLATFORM=wayland to run on Wayland anyway.

解决方法：
	/etc/gdm3/custom.conf #WaylandEnable=false 删除这个# reboot













