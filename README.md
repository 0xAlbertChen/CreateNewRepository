# 将已有项目代码通过命令行方式上传到github，傻瓜教程（图文）

本文地址：http://www.jianshu.com/p/6030066a20e4

# 1. 创建一个github项目

打开www.github.com注册你自己的账号，登陆后点击右上角的 （+）按钮，然后点击new Repository，如下图所示

![创建一个新的Repository](http://upload-images.jianshu.io/upload_images/1552893-9e7c14bc708fe560.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


# 2. 在Repository name处填写项目的名字，并点击 Create Repository，如下图


![填写Repository的名字.png](http://upload-images.jianshu.io/upload_images/1552893-75c2a94f90a04a00.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

# 3. 点击Clone or download，点击Copy to clipboard图标，如下图

![复制git地址.png](http://upload-images.jianshu.io/upload_images/1552893-81a76584d5c64629.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


# 4. 创建并切换到你的工作目录 我用的是~/Documents/2018code


```
mkdir -p ~/Documents/2018code
cd ~/Documents/2018code
```
![image.png](http://upload-images.jianshu.io/upload_images/1552893-9d8a227f9efff163.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



# 5. 把创建好的项目克隆下来

```
git clone https://github.com/xy83918/CreateNewRepository.git
```

![image.png](http://upload-images.jianshu.io/upload_images/1552893-6cb2201d76c5cf9f.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)




# 6. 查看目录，并切换到新建目录


```
ls
cd CreateNewRepository/
```


![image.png](http://upload-images.jianshu.io/upload_images/1552893-9f291fc119d384fe.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


![image.png](http://upload-images.jianshu.io/upload_images/1552893-c3e1fc20553c394c.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



# 7. 将已有的项目copy到这个目录下面



小技巧可以使用 open . 使用finder打开当前目录，然后把你想要添加的文件拖动到这个目录就可以了
open . 

![image.png](http://upload-images.jianshu.io/upload_images/1552893-a1685dad115c62f1.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



####检查一下目录是否有改动


```
git status
```
![image.png](http://upload-images.jianshu.io/upload_images/1552893-ed2b06279dd5ef74.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


####创建一个文件


```
echo “# test” >> test.txt

```
![image.png](http://upload-images.jianshu.io/upload_images/1552893-d98e3ad7ce2c4e47.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


####再次检查一下目录是否有改动


```
git status
```
![image.png](http://upload-images.jianshu.io/upload_images/1552893-9cc98d16f50bcc72.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



# 8. 添加、提交、合并代码



```
git add -A

git commit -m "add test.txt"

git push origin master
```

![image.png](http://upload-images.jianshu.io/upload_images/1552893-0e6adb93f494b212.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)





# 9. 去github上查看新创建的文件已经上传上来了

![image.png](http://upload-images.jianshu.io/upload_images/1552893-614c121e90a0df94.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

# 10 . One more thing 我们再来一次，添加点好玩的

![image.png](http://upload-images.jianshu.io/upload_images/1552893-3e0a4a2574f09b35.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

贴出来方便大家粘贴

```
AlbertMP:CreateNewRepository Albert$ echo "这是一个网页" >> index.html
AlbertMP:CreateNewRepository Albert$ ls
README.md	index.html	test.txt
AlbertMP:CreateNewRepository Albert$ git add -A
AlbertMP:CreateNewRepository Albert$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	new file:   index.html

AlbertMP:CreateNewRepository Albert$ git commit -m "init"
[master 779e7e9] init
 1 file changed, 1 insertion(+)
 create mode 100644 index.html
AlbertMP:CreateNewRepository Albert$ git push origin master
Counting objects: 3, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 318 bytes | 318.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/xy83918/CreateNewRepository.git
   163303f..779e7e9  master -> master
AlbertMP:CreateNewRepository Albert$
```

## 将我们的静态网页发布


###点击Settings
![image.png](http://upload-images.jianshu.io/upload_images/1552893-546883db2634b319.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


### 滚动到GitHub Pages

![image.png](http://upload-images.jianshu.io/upload_images/1552893-f695574c222b31ee.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### 设置成和下图一样

![image.png](http://upload-images.jianshu.io/upload_images/1552893-ef747a28505c0529.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

###点击链接，你的静态网站生成了

![image.png](http://upload-images.jianshu.io/upload_images/1552893-cd512ec1e9c7c41d.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

然后你就可以为所欲为了，想做什么静态网页都可以去修改这个html了。

https://xy83918.github.io/CreateNewRepository/


