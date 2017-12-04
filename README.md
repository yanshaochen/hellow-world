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
修改内层pem.xml的<artifactId>和<name>
修改外层pom.xml的<modules>
modules中移除原先的Artifacts,添加需要的artifacts->web application exploded
配置tomcat
运行！
