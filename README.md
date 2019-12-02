# njit8021xclient_for_Openwrt
## 描述： 
        这是liuqun大佬写的Makefile，用来在Openwrt中编译njit8021xclient。福建农林大学inode7亲测可用。相关源码请点击[这里](https://github.com/TUT123456/njit8021xclient.git)
## 用法：
        - 编写Openwrt源码的feeds.conf
                1. cp feeds.conf.default feeds.conf
                2. vi feeds.conf
                3. 最后一行加上：src-git njit8021xclient https://github.com/TUT123456/njit8021xclient_for_Openwrt.git
        - 更新下载拓展包
                ./scripts/feeds update -a
                ./scripts/feeds install -a
        - 最后在menuconfig里面勾选njit8021x即可
