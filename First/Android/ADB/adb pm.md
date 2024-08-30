1.查看当前连接设备或者虚拟机的所有包

adb shell pm list packages

2.只输出系统的包

adb shell pm list packages -s

3.输出所有第三方包

adb shell pm list packages -3

4.输出包和包相关联的文件(安装路径)

adb shell pm list packages -f

5.输出包和安装信息（安装来源）

adb shell pm list packages -i

6.输出包含过滤条件的包

adb shell pm list packages “lzy”

7.只输出启用的包

adb shell pm list packages -e

8.只输出禁用的包

adb shell pm list packages -d

9.只输出包和未安装包信息（安装来源）

adb shell pm list packages -u
————————————————

                            版权声明：本文为博主原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接和本声明。
                        
原文链接：https://blog.csdn.net/wxd_csdn_2016/article/details/103145753