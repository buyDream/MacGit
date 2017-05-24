Git 简单使用

1. 在制定路径建立空目录

   cd  <路径>

   mkdir <文件夹名>     #新建文件夹名称

   cd  <文件夹名>   # 

2. git init  # 初始化仓库

   ![屏幕快照 2017-05-24 下午2.17.01](/Users/refrain/Desktop/屏幕快照 2017-05-24 下午2.17.01.png)

   仓库此时便创建好了，并且告诉你是个空仓库



3. 在目录下创建文件

   touch README.md    #

   open README.md  # 打开文件进行编辑（也可使用vim 编辑）



​	3.1完成编辑后，可使用git status查看当前git仓库的状态

![屏幕快照 2017-05-24 下午2.27.39](/Users/refrain/Desktop/屏幕快照 2017-05-24 下午2.27.39.png)

可看到，有三个文件处于untracked状态，



4. 添加到缓存区

   git add README.md 

   4.1 查看状态

   git status

   ![屏幕快照 2017-05-24 下午2.36.12](/Users/refrain/Desktop/屏幕快照 2017-05-24 下午2.36.12.png)

这里就到最后一步了，

​	4.1    git diff --cached   查看缓存区那些文件被修改

​		如果发现文件显示不全，按方向键↓显示更多，退出输入q

5. 提交到本地

   git commit -m "create one file"

![屏幕快照 2017-05-24 下午2.51.23](/Users/refrain/Desktop/屏幕快照 2017-05-24 下午2.51.23.png)

再次查看状态，没有需要commit的，缓存区也被清空

​	5.1 如果遇到![屏幕快照 2017-05-24 下午2.59.46](/Users/refrain/Desktop/git使用/屏幕快照 2017-05-24 下午2.59.46.png)

​	可以忽视，最好配置一下

​	

​	5.1 也可使用以下语句提交，它会将没有添加到缓存区的修改也一起提交，但不会添加新建的文件。

​	如，我新建了一个文件newfile.txt，并不把他添加到缓存区![屏幕快照 2017-05-24 下午3.13.54](/Users/refrain/Desktop/屏幕快照 2017-05-24 下午3.13.54.png)

​	在将README.md修改的添加到缓存区

​	再次修改README.md（为了验证没有添加到缓存区的修改）

​	查看状态

![屏幕快照 2017-05-24 下午3.03.08](/Users/refrain/Desktop/git使用/屏幕快照 2017-05-24 下午3.03.08.png)



​	提交

​	__git commit -a -m "create newfile.txt 2. modified README.md"__

​	再次查看状态![屏幕快照 2017-05-24 下午3.03.39](/Users/refrain/Desktop/git使用/屏幕快照 2017-05-24 下午3.03.39.png)

​	修改的部分提交成功了，新建的文件没有成功提交



# 进阶了

