
workon: 打印所有的虚拟环境；
mkvirtualenv xxx: 创建 xxx 虚拟环境，可以–python=/usr/bin/python3.6 指定python版本;
workon xxx: 使用 xxx 虚拟环境;
deactivate: 退出 xxx 虚拟环境；
rmvirtualenv xxx: 删除 xxx 虚拟环境。
lsvirtualenv : 列举所有的环境。
cdvirtualenv: 导航到当前激活的虚拟环境的目录中，比如说这样您就能够浏览它的 site-packages。
cdsitepackages: 和上面的类似，但是是直接进入到 site-packages 目录中。
lssitepackages : 显示 site-packages 目录中的内容。