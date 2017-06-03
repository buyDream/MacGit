上传代码到GitHub出现

~~~shell
RefrainingdeMacBook-Pro:my_ez_blog refrain$ git push -u origin master
ssh: Could not resolve hostname github.com: nodename nor servname provided, or not known
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
	
~~~

时：

#### 1.原因

没有在GitHub账号下添加SSH key

#### 2.解决方法

在终端

##### 2.1创建SSH key

~~~shell
$ ssh-keygen -t rsa -C "refrainGo"
Generating public/private rsa key pair.
Enter file in which to save the key (/Users/refrain/.ssh/id_rsa): 
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in /Users/refrain/.ssh/id_rsa.
Your public key has been saved in /Users/refrain/.ssh/id_rsa.pub.
The key fingerprint is:
~~~

遇到几个冒号，要你输入什么东西时，直接回车就好了，总共有三个地方需要回车。应该就创建好了，注意：__Your public key has been saved in__ 后面就是存放的路径

##### 2.2查看SSH key

~~~shell
$ cat /Users/refrain/.ssh/id_rsa.pub 
ssh-rsa AAAAB3XXXXXXX
XXXXX
#.....中间省略
yAgZiCH5 refrainGo
~~~



##### 2.3打开GitHub账号添加SSH key

###### 	2.3.1 登录GitHub账号

###### 	2.3.2点击右上方（头像）Settings

###### 	2.3.3选择左侧SSH and GPG keys

###### 	2.3.4点击 New SSH key

​		为该key写上可辨认的title，然后把本地查看的SSK key全部复制过来，再点击Add SSH key即可。

##### 2.3 重新上传就好了

~~~shell
$ git push -u origin master
~~~



