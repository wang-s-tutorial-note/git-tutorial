# github 用户验证机制

> github给开了私人仓库，普通推送回显示找不到仓库。

# 创建私钥链接github

1.ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

2. eval "$(ssh-agent -s)"

3. vi .ssh/config

Host *
  AddKeysToAgent yes
  UseKeychain yes  // 在服务器要去掉
  IdentityFile ~/.ssh/id_rsa

4. ssh-add -K ~/.ssh/id_rsa

5.验证是否成功

ssh -T git@github.com


# 如何连接pricate仓库

`git init ` build a work area.

    only  you add the ssh key that you can push the public repository $$ .only you add the 
    usrname and password then authorized you have the identify , therefore you can use the 
    private repository.

`git remote rm origin`
`git remote add origin  https://usrname:password@github.com/usrname/repositoryname.git`
