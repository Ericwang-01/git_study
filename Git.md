# Git

- 版本迭代

- 分布式版本控制/集中版本控制  SVN
  
  <img title="" src="file:///C:/Users/ryin/AppData/Roaming/marktext/images/2023-03-30-10-00-07-image.png" alt="" width="365"><img title="" src="file:///C:/Users/ryin/AppData/Roaming/marktext/images/2023-03-30-10-00-44-image.png" alt="" width="428">

### 四个区域

![](C:\Users\ryin\AppData\Roaming\marktext\images\2023-03-30-09-58-52-image.png)

- Workspace：工作区，就是你**平时存放项目代码**的地方

- Index / Stage：暂存区，用于**临时存放你的改动**，事实上它只是一个文件，保存即将提交到文件列表信息

- Repository：本地仓库，就是安全存放数据的位置，这里面有你提交到**所有版本**的数据。其中HEAD指向最新放入仓库的版本

- Remote：远程仓库，托管代码的服务器，可以简单的认为是你项目组中的一台电脑用于远程数据交换

### 本地的三个区域

本地的三个区域确切的说应该是git仓库中HEAD指向的版本：

![Image](https://mmbiz.qpic.cn/mmbiz_png/uJDAUKrGC7Ksu8UlITwMlbX3kMGtZ9p0icz6X2aibIgUWzHxtwX8kicPCKpDrsiaPzZk04OlI2bzlydzicBuXTJvLEQ/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)

- Directory：使用Git管理的一个目录（仓库）=工作空间+Git的管理空间。

- WorkSpace：需要通过Git进行版本控制的目录和文件

- .git：存放Git管理信息的目录，初始化仓库的时候自动创建。

- Index/Stage：暂存区，在提交进入repo之前，我们可以把所有的更新放在暂存区。

- Local Repo：本地仓库，一个存放在本地的版本库；HEAD会只是当前的开发分支（branch）。

- Stash：隐藏，是一个工作状态保存栈，用于保存/恢复WorkSpace中的临时状态。

# 工作流程

１、在工作目录中添加、修改文件；

２、将需要进行版本管理的文件放入暂存区域（git add .）；

３、将暂存区域的文件提交到git仓库(git commit)。

因此，git管理的文件有三种状态：已修改（modified）,已暂存（staged）,已提交(committed)

![Image](https://mmbiz.qpic.cn/mmbiz_png/uJDAUKrGC7Ksu8UlITwMlbX3kMGtZ9p09iaOhl0dACfLrMwNbDzucGQ30s3HnsiaczfcR6dC9OehicuwibKuHjRlzg/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)

# Git项目搭建

![Image](https://mmbiz.qpic.cn/mmbiz_png/uJDAUKrGC7Ksu8UlITwMlbX3kMGtZ9p0AII6YVooUzibpibzJnoOHHXUsL3f9DqA4horUibfcpEZ88Oyf2gQQNR6w/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)

- 两种同步方式
  
  - 搭建本地仓库
  
  - 克隆远程仓库

- 代码修改修改完成后
  
  - `git add . `将当前目录添加到暂存区；
  
  - `git status `查看是否添加成功；
  
  - ` git commit `提交到本地仓库；

- 忽略文件 `.gitignore`
1. 忽略文件中的空行或以井号（#）开始的行将会被忽略。

2. 可以使用Linux通配符。例如：星号（*）代表任意多个字符，问号（？）代表一个字符，方括号（[abc]）代表可选字符范围，大括号（{string1,string2,...}）代表可选的字符串等。

3. 如果名称的最前面有一个感叹号（!），表示例外规则，将不被忽略。

4. 如果名称的最前面是一个路径分隔符（/），表示要忽略的文件在此目录下，而子目录中的文件不忽略。

5. 如果名称的最后面是一个路径分隔符（/），表示要忽略的是此目录下该名称的子目录，而非文件（默认文件或目录都忽略）。
   
   ---
   
   - `[]`：内的内容是可选的
   
   - `{}`：一组必须的项目，必须要在{a|b|c}内给出的选择里选一个。
   
   - `<>`：表示必须被替换的占位

> 1，一个系统的教程重要，要有背后的原理和落地的操作命令以及完整的工作流程
> 
> 2，经常用`--help`查看官方文档
> 
> 3，查看当前状态的命令很重要，如：`git status` , ` git branch`, `pwd` , ` ls` , ` tree`
