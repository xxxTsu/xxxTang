## 下载安装
+ https://git-scm.com/download/win
+ 安装,下一步下一步

## 初始化配置
+ 初始化用户信息

```shell

 // 设置用户名
git config --global user.name "John Doe"
 // 设置邮箱
git config --global user.email "johndoe@example.com"
// 查看配置项
git config --list

```

## 命令
+ git init  对文件夹进行初始化,变成工作区
+ git add .   把工作区所有内容提交到暂存区
+ git status   查看文件状态
  - 显示绿色的,说明文件都被提交到了暂存区
  - 显示红色的文件,说明在工作区有变动,而且没有被提交到暂存区
+ git checkout 文件名  把暂存区的某个文件还原
  - 会覆盖工作区的内容,谨慎使用!
+ git commit -m'提交描述'   把暂存区内容,提交到存储区
  - 不能跨步骤处理,不能直接从工作区执行commit
  - 提交到存储区会形成一个版本,由唯一的hash值来标识
  - 如果没有输入-m则会默认进入一个vm编辑器,需要用命令 :wq  回车才能退出

+ git log   查看提交到存储区的内容日志
+ git reset --hard 'hash'  乘坐时光机回到某个版本


## 远程仓库
+ git remote add origin 远程仓库地址
  - 关联本地和远程仓库
+ git remote -v  查看远程关联信息
+ git push -u origin "master"   把本地代码推送到远程"master"分支
  - 这个命名仅限第一次推送,因为携带了-u 意思是记住我
  - 下次直至执行git push 即可
+ git clone   xxx.git  克隆远程仓库到本地
+ git push  如果以前提交了-u,标识已经默认知道往哪提交了
  - 如果两个人同时修改了同一个文件,会造成冲突
  - 如果提示冲突,需要先git pull合并代码后再提交
+ git pull  origin master  把远程master分支内容拉下来

## 配置本地密钥
+ ssh-keygen -t rsa -C "你的邮箱地址"
  - 注意 需要去远程仓库个人中心,配置ssh,把本地生成的id_rsa.pub文件内容配置进去


