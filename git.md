# git基本操作
$ git config -l	//查看配置信息  
$ git config --global user.name "sophotomato"	//设置全局user name  
$ git config --global user.email johndoe@example.com  

## git仓库初始化
$ git init

## 添加跟踪文件，并提交
$ git add *.c  
$ git add README  
$ git commit -m 'initial project version'  
注：commit提交add内容，包括文件修改和新添加的跟踪文件  

## 仓库clone
$ git clone git://github.com/sophotomato/sophotomato.github.io.git



## 检查当前文件状态
$ git status


文件 .gitignore 的格式规范如下：

	所有空行或者以注释符号 ＃ 开头的行都会被 Git 忽略。
	可以使用标准的 glob 模式匹配。
	匹配模式最后跟反斜杠（/）说明要忽略的是目录。
	要忽略指定模式以外的文件或目录，可以在模式前加上惊叹号（!）取反。



## 比较已暂存(git add)和未暂存的内容
$ git diff

## 比较暂存和提交的内容
$ git diff --cached
$ git diff --staged	//git 1.6.1 or 更改版本

## 跳过暂存区提交
$ git commit -a


## 移除文件
## 移除删除的文件（以后再也不跟踪这个文件了）
$ git rm <filename>
## 移除add的文件
$ git rm --cached <filename>

## 移动文件
$ git mv README.txt README

## 查看提交历史
$ git log
### 常用 -p 选项展开显示每次提交的内容差异，用 -2 则仅显示最近的两次更新
$ git log -p -2



# 远程仓库
## 要查看当前配置有哪些远程仓库
$ git remote

## 添加远程仓库
$ git remote add test git://github.com/sophotomato.github.io.git
## 获取仓库数据
$ git fetch test
## 推送数据到远程仓库
$ git push test master<branch-name>
## 远程仓库的删除和重命名
$ git remote rename test newtest

# branch 相关内容
## 新建branch
$ git branch testing

##### HEAD 指向当前所在的分支
## 切换分支
$ git checkout testing
## 删除分支
$ git branch -d testing