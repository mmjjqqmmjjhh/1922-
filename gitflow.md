### git flow 
git  sourcetree constone  svn ...
#### 名词解析
git  一个工具
github 远程仓库的集合体 （码云）
git远程仓库  和本地仓库建立连接 上传下拉代码 服务器上
git本地仓库  个人开发者在自己本地创建的仓库   和远程仓库建立连接
git 工作区   本地仓库的 开发者写代码的地方  通过add 指令将修改的代码添加到暂存区
git 暂存区   本地仓库的 暂时储存的区域  临时保存修改的 通过git commit 将修改添加到分支
git 分支     git中最终存储的位置 
#### 基本指令
```
git init  //初始化本地仓库
git clone //远程拉取代码
git status //查看状态
git log  // 打印log信息
git relog // 操作信息
git add  //添加到缓存区
git diff // 比较工作区与暂存区之间的差异
git commit //提交
git branch //展示分支
git checkout //切换分支
git merge   //合并分支
git remote  //查看远程信息
git push origin dev   // 推送分支
git reset  //恢复到之前的某一个版本
git revert  //创建一个新版本与恢复的版本一直
git pull  //拉取最新代码
```
#### gitflow git工作流程

#### 参考资料
[git基本使用](https://www.liaoxuefeng.com/wiki/896043488029600)

##### 本地基本指令
```
git  init 

创建本地仓库

git  add  .    ./文件
将工作区的文件改变 提交到暂存区

git commit  -m '备注'
将暂存区的改变 提交到 分支

git  status  
查看git 仓库的状态

git branch  

查看本地分支

git branch -d 分支名
删除分支  不支持自杀  

git  checkout 分支名
切换已有分支

git  checkout  -b 分支名
创建新的分支并且切换  将当前所在分支做了一份拷贝 形成一个子分支

git  merge 分支名

在当前分支合并某一分支 （母合并子）

git diff  

查看工作区和暂存区的文件改变


git log
打印当前用户操作git的信息 commit 提交操作

git reflog
打印用户的操作信息  合并 切换  提交
``` 
#### 远程仓库相关
1.创建一个远程仓库 github  码云 （公有仓库 私有仓库）  运维创建（gitlab）
 1.2 通过一个 readme 初始化远程仓库
 1.3 git clone  地址 https
2.先通过git init 创建本地仓库
 2.1创建本地仓库和远程仓库的连接关系
   git remote add origin https://github.com/fchangjun/sfjlsfjslfj.git

git  push origin(仓库名)  dev(分支名)
将本地分支提交到线上

git  pull  origin（仓库名）dev（分支名）
下拉代码
##### 合并分支冲突
2个分支相同部分直接合并  不同部分工具无法区分 所以将选择权交给开发者 这就是冲突

需要的留着 不要的删除  -》沟通

##### 忽略文件 .gitignore

#### gitflow
1. 切换分支合并分支

