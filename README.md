# git

有个很好的在线学习网站，推荐给大家： https://learngitbranching.js.org/

![img](https://pdai-1257820000.cos.ap-beijing.myqcloud.com/pdai.tech/public/_images/tool-git-learn-1.png)

## 1.安装

#### 1.1 windows

下载 链接：https://git-scm.com/download/win

#### 1.2 Linux

```
apt install git
```

## 2.同步github

#### 2.1.创建ssh key

ssh-keygen -t rsa -C "你自己注册GitHub的邮箱" 

#### 2.2 github添加key

打开“Account settings”--“SSH Keys”页面，然后点击“Add SSH Key”，填上Title（随意写），在Key文本框里粘贴 id_rsa.pub文件里的全部内容

 id_rsa.pub 默认在C:\Users\Administrator\.ssh

每台想要登陆某个github账号的主机都需要有一个对应的key，例如你有一个github账号，你在你的笔记本和台式上都要创建key

#### 2.3客户端测试

ssh -T git@github.com

#### 3.4登录

git config --global user.name "你的GitHub登陆名"

git config --global user.email "你的GitHub注册邮箱"

#### 3.5 传输到github上

git remote add origin git@github.com:userName/yourProject.git

git add .

git commit -m "tag"

git push -u origin master

