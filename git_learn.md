 # Git教程 #
-------------
```
$git #查看Git是否安装
$ git config --global user.name "Your Name"
$ git config --global user.email "email@example.com"
---------------------------------------------------------------------------------
$mkdir learngit #创建一个新的版本库
$cd learngit #进入这个版本库
$git add readme.txt #向版本库提交一个txt文件，且该文件需要放在learngit文件夹下
$git commit -m "Wrote a readme file"#把文件提交到仓库
$git status #查看版本库当前的状态
$git log #查看历史记录
$git log --pretty=oneline #查看简洁版本的历史记录
$git reset --hard HEAD^ #当前版本为Head，^表示返回到上一个版本，^^表示返回到上两个版本，依此类推
$cat readme.txt #查看文件内容
$git reflog #用来记录每一次命令



```

