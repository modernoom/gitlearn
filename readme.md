# git学习
1. ##### git简介
    + Git是目前世界上最先进的分布式版本控制系统 能记录每次文件的改动
    + git 是linus 用c语言写的一个版本控制系统
    + 2008年，GitHub网站上线了，它为开源项目免费提供Git存储，无数开源项目开始迁移至GitHub，包括jQuery，PHP，Ruby等等。
2. ##### 集中式与分布式
    + 集中式
      
        > 集中式版本控制系统，版本库是集中存放在中央服务器的，而干活的时候，用的都是自己的电脑，所以要先从中央服务器取得最新的版本，然后开始干活，干完活了，再把自己的活推送给中央服务器。集中式版本控制系统最大的毛病就是必须联网才能工作.
    + 分布式
        >分布式版本控制系统根本没有“中央服务器”，每个人的电脑上都是一个完整的版本库，这样，你工作的时候，就不需要联网了，因为版本库就在你自己的电脑上。
        > 既然每个人电脑上都有一个完整的版本库，那多个人如何协作呢？比方说你在自己电脑上改了文件A，你的同事也在他的电脑上改了文件A，这时，你们俩之间只需把各自的修改推送给对方，就可以互相看到对方的修改了。
        > 和集中式版本控制系统相比，分布式版本控制系统的安全性要高很多，因为每个人电脑里都有完整的版本库，某一个人的电脑坏掉了不要紧，随便从其他人那里复制一个就可以了。
        > 在实际使用分布式版本控制系统的时候，其实很少在两人之间的电脑上推送版本库的修改，因为可能你们俩不在一个局域网内，两台电脑互相访问不了，也可能今天你的同事病了，他的电脑压根没有开机。因此，分布式版本控制系统通常也有一台充当“中央服务器”的电脑，但这个服务器的作用仅仅是用来方便“交换”大家的修改，没有它大家也一样干活，只是交换修改不方便而已。

3. ##### windows安装git
    + 安装 在Windows上使用Git，可以从Git官网直接下载安装程序，然后按默认选项安装即可。
    + 安装完成后，在搜索git找到“Git”->“Git Bash”，蹦出一个类似命令行窗口的东西，就说明Git安装成功
    + 设置，打开bash后在命令行中输入:
```
$ git config --global user.name "你的名字"
$ git config --global user.email "邮箱地址"
```
     注意git config命令的--global参数，用了这个参数，表示你这台机器上所有的Git仓库都会使用这个配置   
4. ##### 创建版本库
    + 版本库又名仓库，英文名repository，你可以简单理解成一个目录，这个目录里面的所有文件都可以被Git管理起来，每个文件的修改、删除，Git都能跟踪，以便任何时刻都可以追踪历史，或者在将来某个时刻可以“还原”。
    1. 使用mkdir 文件夹名  命令创建1个空目录(用来存放repository)
    2. cd 文件夹名 进入文件夹
    3. 通过git init命令把这个目录变成Git可以管理的仓库,当前目录会多一个.git的目录，这个目录是Git来跟踪管理版本库的。
    4. 将文件放置在该仓库目录下 
    5. 使用命令git add 文件名称，注意，可反复多次使用，添加多个文件；  
    6. 使用命令git commit -m "提交信息"，完成。



