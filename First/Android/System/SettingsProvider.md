参考[连接](https://www.jianshu.com/p/d48977f220ee)
上面的代码中对Global、System、Secure分别生成一个File对象实例，它们的File对象分别对应的文件是：

- /data/system/users/0/settings_global.xml
- /data/system/users/0/settings_system.xml
- /data/system/users/0/settings_secure.xml

与[[SystemProperties]]相比
SettingsProvider有点类似Android的properties系统（Android属性系统）：SystemProperties。SystemProperties除具有SettingsProvider以上的三个特性，SettingsProvider和SystemProperties的不同点在于：

- 数据保存方式不同：SystemProperties的数据保存属性文件中（/system/build.prop等），开机后会被加载到system properties store；SettingsProvider的数据保存在文件/data/system/users/0/settings_***.xml和数据库settings.db中；
- 作用范围不同：SystemProperties可以实现跨进程、跨层次调用，即底层的c/c++可以调用，java层也可以调用；SettingProvider只能能在java层（APP）使用；
- 公开程度不同：SettingProvider有部分功能上层第三方APP可以使用，SystemProperties上层第三方APP不可以使用。