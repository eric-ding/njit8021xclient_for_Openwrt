# njit8021xclient_for_Openwrt
## 这是liuqun大佬写的Makefile，用来在Openwrt中编译njit8021xclient！！！
## 用法：
        - 编写Openwrt源码的feeds.conf
            1. cp feeds.conf.default feeds.conf
            2. vi feeds.conf
            3. 最后一行加上：src-svn njit https://github.com/TUT123456/njit8021xclient_for_Openwrt\njit8021xclient
        - make menuconfig里面勾选njit8021xclient
