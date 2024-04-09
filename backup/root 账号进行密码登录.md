![root](https://github.com/8355577/hyc/assets/48672935/01956286-bdce-46f5-bfda-fd3434c6d776)

开的服务器，只能用证书登录而不能用 root 账号进行密码登录。我个人习惯不好，喜欢直接 root 账号密码登录，请各位不要学我。

需求：打开 root 账户的密码登录功能。

查了一下资料，设置这个很简单。

设置方式
终端执行命令行
`sudo vi /etc/ssh/sshd_config`
然后按 Insert 进如编辑模式，方向键上下左右找到 PermitRootLogin 和 PasswordAuthentication 进行修改
`PermitRootLogin yes`
`PasswordAuthentication yes`
然后执行
`sudo service sshd reload`
更改密码
`sudo passwd root`
