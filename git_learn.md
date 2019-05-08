 # Git教程 #
-------------

```
$git #查看Git是否安装
$ git config --global user.name "Your Name"
$ git config --global user.email "email@example.com"
---------------------------------------------------------------------------------
$mkdir learngit #创建一个新的版本库
$cd learngit #进入这个版本库
$git init #将这个版本库变为git可以管理的版本库
$git add readme.txt #向版本库提交一个txt文件，且该文件需要放在learngit文件夹下
$git commit -m "Wrote a readme file"#把文件提交到仓库
$git status #查看版本库当前的状态
$git log #查看历史记录
$git log --pretty=oneline #查看简洁版本的历史记录
$git reset --hard HEAD^ #当前版本为Head，^表示返回到上一个版本，^^表示返回到上两个版本，依此类推
$cat readme.txt #查看文件内容
$git reflog #用来记录每一次命令
--------------------------------------------------------------------------------
```
### 工作区和暂存区 ###
* 工作区：learngit文件夹
* 版本库：生成的.git隐藏文件夹

工作原理：
```
$git add readme.txt #将工作区中的readme.txt添加到暂存区
$git commit -m "Wrote a readme file" #将暂存区的文件放到版本库的master分支
#每一次在工作区中将文件修改后都要用git add将其添加到版本库，再用git commmit -m将其保存到
master分支
$git checkout --readme.txt #弃置工作区的修改，分两种情况，第一种是在工作区修改后未使用
git add添加到暂存区，此时会恢复到和之前版本库一模一样的情况；第二种是添加到暂存区后又进行了
修改，此时恢复到之前添加到暂存区的情况
$git reset HEAD readme.txt #将放到暂存区的文件修改清除，并放回到工作区
#如果说已经commit了，那么就进行版本回退，千万不要提交到远程，否则真的无计可施！！！
$git add test.txt
$rm test.txt #从工作区中删除test文件
$git rm test.txt #从版本库中同步删除test.txt
$git commit -m "delete test.txt"
$git checkout -- test.txt #当工作区删错时，将版本库的文件同步到工作区
```
### 远程仓库 ###
```
#首先在本地创造一个仓库，在github create一个repository
$git remote add origin git@github.com:SaoirseSun/git_learn.git
#若报错origin已存在，则先$git remote rm origin再进行同样操作
$git push -u origin master #


```