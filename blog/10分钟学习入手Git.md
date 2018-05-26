> 创建秘钥

&nbsp;


```javascript
ssh-keygen -t rsa -b 4096 -c "邮箱地址"
```

![clipboard.png](https://upload-images.jianshu.io/upload_images/12361527-17e473b4c74762a8.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

> github添加远程公钥

&nbsp;
 
![clipboard1.png](https://upload-images.jianshu.io/upload_images/12361527-1514fa20f9959c56.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

> 克隆远程仓库

&nbsp;

![clipboard2.png](https://upload-images.jianshu.io/upload_images/12361527-2447d2141041517c.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![clipboard3.png](https://upload-images.jianshu.io/upload_images/12361527-71eb4dd4c1d0a202.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![clipboard4.png](https://upload-images.jianshu.io/upload_images/12361527-9db313d0754b45a9.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

> clone 项目

用于把GitHub上的项目克隆到本地变为本地仓库

```javascript
git clone git@github项目地址
```

> 添加项目并提交

&nbsp;

```javascript
# 创建新文件
touch 1.html

# 将当前目录的所有文件提及到缓存区
git add .
git commit -am "xxxx"

# 推送到远程仓库
git push xxx master
```

## **本地创建一个git项目并提交到GitHub的空仓库**

&nbsp;

> github上先添加一个空仓库

&nbsp;

![clipboard5.png](https://upload-images.jianshu.io/upload_images/12361527-da46f8b4ac382fa2.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![QQ截图20180526182552.png](https://upload-images.jianshu.io/upload_images/12361527-1eb81aa984299147.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

> 本地创建一个git项目

&nbsp;

```javascript
# 创建目录
mkdir resume
cd resume

# 初始化仓库
git init

# 创建一些文件或者目录
mkdir blog
touch blog/10分钟学习入手Git.md
touch blog/使用Markdown写文章.md

mdkir projects
touch projects/demo1.html

touch README.md

# 配置远程仓库地址并设置标签,这里设置了一个resume标签
git remote add resume git@github.com:zhangcl0531/resume.git

# 查看当前本地库记录的远程仓库
$ git remote -v
resume  git@github.com:zhangcl0531/resume.git (fetch)
resume  git@github.com:zhangcl0531/resume.git (push)

# 提交
git add .
git commit -am "xxxx"
git push resume  master
```

![QQ截图20180526184352.png](https://upload-images.jianshu.io/upload_images/12361527-8214bd6fec6b0e5f.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

> 删除修改标签

&nbsp;

```javascript
# 删除本地仓库的远程仓库
git remote remove 标签名

# 修改远程仓库标签名
git remote rename 原标签名 新标签名

# 修改远程仓库地址
git remote set-url 标签名  新的远程仓库地址
```

> 分支操作

&nbsp;

```javascript
# 创建本地库dev 分支
git branch dev

# 切换到dev分支
git checkout dev

# 推送更新到dev分支
git push 标签名 dev

# 查看所有分支，带* 表示当前所在位置
git branch -a

# 合并分支，先切换到master，再合并
git checkout master
# 将dev分支合并当当前master分支上
git merge dev 


```