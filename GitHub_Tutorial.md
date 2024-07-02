# <center> GitHub快速入门

点击此是<a href="https://github.com/" title="超链接title">网站地址</a>

## 注册

![image-20240702165811968](C:\Users\89548\AppData\Roaming\Typora\typora-user-images\image-20240702165811968.png)

直接就一步一步注册就可以了



## 本地和仓库的绑定

![image-20240702165849672](C:\Users\89548\AppData\Roaming\Typora\typora-user-images\image-20240702165849672.png)

这是我创的仓库，大家都得把这个远程仓库和自己本地的文件绑定，方便以后更新pull和上传push。所以首先大家得先下载Git Bash这个工具：

![image-20240702170011126](C:\Users\89548\AppData\Roaming\Typora\typora-user-images\image-20240702170011126.png)

### 下载Git Bash

下载地址：[Git - Downloads (git-scm.com)](https://www.git-scm.com/download/)



下载的时候就默认一直next就行。

下载完如果右键可以看到这个(Open Git Bash here) 就说明下载成功了：

![96d233d599ea453ccc3d3400c26c98c](D:\WeChat Files\wxid_0tbenc9swjb611\FileStorage\Temp\96d233d599ea453ccc3d3400c26c98c.jpg)



### 本地获取ssh绑定github账号

我们建一个文件夹，然后在这个文件夹中右键Open Git Bash here,弹出来这个窗口，以我的为例：

![image-20240702170453930](C:\Users\89548\AppData\Roaming\Typora\typora-user-images\image-20240702170453930.png)

然后在命令行里面输入：

```
ssh-keygen -t rsa -C "你的github账号"
```

然后就按照他的指示选择你存ssh的文件夹，密码，成功后会弹出来这些信息

![image-20240702170645917](C:\Users\89548\AppData\Roaming\Typora\typora-user-images\image-20240702170645917.png)

你可以在电脑文件夹里查看这些ssh

![image-20240702170758766](C:\Users\89548\AppData\Roaming\Typora\typora-user-images\image-20240702170758766.png)

用记事本打开id_rsa.pub,把里面的内容全部复制一下：

![image-20240702170835660](C:\Users\89548\AppData\Roaming\Typora\typora-user-images\image-20240702170835660.png)

打开github，在个人设置里面打开这个：

![image-20240702170911658](C:\Users\89548\AppData\Roaming\Typora\typora-user-images\image-20240702170911658.png)

添加ssh key（我已经添加过了所以已经有显示了。)

添加成功后可以输入查看是否绑定成功：

```
ssh -T git@github.com
```

成功会出现下面的信息：

![image-20240702171245820](C:\Users\89548\AppData\Roaming\Typora\typora-user-images\image-20240702171245820.png)

输入下两行代码来设置一下本地的config文件：

```
$ git config --global user.user "你的账号"
$ git config --global user.email "你注册的邮箱"
```

![image-20240702171354781](C:\Users\89548\AppData\Roaming\Typora\typora-user-images\image-20240702171354781.png)

### 本地克隆

我们的仓库ssh地址：git@github.com:skyhappyctl/Dragon-Circuit-Design-Competition.git（待会直接复制就行）

我们输入：

```
$ git clone git@github.com:skyhappyctl/Dragon-Circuit-Design-Competition.git
```

然后等待克隆完成，就会发现本地有了这个文件夹：

![image-20240702171943306](C:\Users\89548\AppData\Roaming\Typora\typora-user-images\image-20240702171943306.png)

![image-20240702171936988](C:\Users\89548\AppData\Roaming\Typora\typora-user-images\image-20240702171936988.png)

这样就把东西拷下来啦！



### 本地上传文件

比如我要把这个教程文件传上去，首先在这个文件所在的文件夹右键打开这个bash命令行窗口，然后输入：



```
$ git add 文件名
$ git commit -m "写一下你这次push的原因，随便写啥都行"
$ git push origin main
```



然后等待他上传应该就可以啦~

