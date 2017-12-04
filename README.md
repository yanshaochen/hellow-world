# hellow-world
just a repository
make some differents
second change
//how to submit your project
1.use idea create local repository
2.use Git Bash in windows
cd c:/your/local/repository/directory
git remote add origin https://github.com/yanshaochen/hellow-world.git
git pull --rebase origin master
git push -u origin master
3.return to idea add,commit,push 

下载demo后，先删除远程仓库关联：
查看当前仓库的远程仓库
git remote -v
删除所有远程仓库
git remote rm origin
修改外层项目名
修改内层module名和目录名
修改内层pom.xml的<artifactId>和<name>
修改外层pom.xml的<modules>
modules中移除原先的Artifacts,添加需要的artifacts->web application exploded
配置tomcat
运行！

###############################################################################
1）git是分布式的，svn是集中式的
2）git每个历史版本存储完整的文件，svn存储文件的差异
3）git可离线完成大部分操作，svn则必须与中央服务器进行网络交互
4）git有着优雅的分支和合并的功能
5）git有着更强大的撤销修改和修改版本历史的能力
6）git速度更快

git安装 centOS yum install git
which -a git
git version

基本配置：
user.name & user.email

git config user.name  获取当前用户名
git config --list --global  获取全局信息
git config --list 查询所有

添加user.name 和email
git config --global user.name abc
git config --global user.email abc@163.com

git config --global --unset user.name //删除所有user.name
vim ~/.gitconfig  //查看修改配置文件

############创建本地仓库############
git init 在目录下创建一个空的仓库.git目录
touch abc.txt 在仓库目录下创建一个文件
git status  查看当前版本库的状态
1.git add abc.txt  告诉git,把文件添加到仓库
2.git commit -m '第一次提交'   提交到仓库
git只能管理文件类型的数据

diff  比较工作区和暂存区的区别
git diff
git diff abc.txt
结果：
diff --git a/abc.txt b/abc.txt
index e69de29..1376c03 100644
--- a/abc.txt
+++ b/abc.txt
@@ -0,0 +1 @@
+xfdaskldfjas

git log //查所有
git log --pretty=oneline  //好看的查询
git log --pretty=oneline abc.txt   //查看commit id SHA-1 hash计算出的16进制编码
结果（Head是当前版本）：
53747a8c163553f5e445d30b9fe8a7791a52352f (HEAD -> master) 3commit
bf71af2c1a356c42fd842e6379990337f159144b 2commit
84427cfe873664c700a728fc678129b5a20f5041 第一次提交

版本回退（只是移动HEAD指针）：
HEAD^前一个版本，N个前版本 HEAD~N
git reset --hard HEAD^    //回退到上一个版本（第二版）
想回到回退之前的某个版本：
git reset --hard 53747a8c163553f5e445d30b9fe8a7791a52352f   //又回到了第三版
git reset --hard xxx：版本穿梭可以使用git log 查看提交历史（HEAD及以前的版本）

万一忘记了之后的码怎么办？
git reflog  //查看历史版本

