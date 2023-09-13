git 状态查看指令，查看项目当前状态，哪些未提交。
```
$ git status
```
git diff顾名思义就是查看difference，显示的格式正是Unix通用的diff格式
```
git diff readme.txt 
```
git log 查看版本提交记录
```
git log
```
`git checkout -- file`可以丢弃工作区的修改：
```
$ git checkout -- readme.txt
```
`git checkout`命令加上`-b`参数表示创建并切换，相当于以下两条命令：
```
$ git checkout -b dev
Switched to a new branch 'dev'

```
```
$ git branch dev
$ git checkout dev
Switched to branch 'dev'
```
然后，用`git branch`命令查看当前分支：

```
$ git branch
* dev
  master
```