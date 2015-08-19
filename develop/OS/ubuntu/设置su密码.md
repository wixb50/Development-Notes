##Ubuntu设置su密码的命令  
Ubuntu安装之默认状态下是不能使用su命令了，如果我们要使用su命令需要把root设置一个密码这样就可以使用su命令了。    
#### 使用sudo  
$:sudo passwd  
系统提示输入密码，即安装时的用户密码，然后，系统提示输入两次新密码，输入完毕后，  
$:su  
即可进入su，具备了相应的权限了.  

####给root用户设置密码的具体步骤：  
1.打开一个terminal，然后输入下面的命令：  
sudo passwd  
回车后会出现让你输入原始密码，新密码和确认密码  
[sudo] password for you ：---> 输入你的密码（你现在这个用户的密码），密码不会显示。  
Enter new UNIX password: --- > 输入新的 su 密码  
Retype new UNIX password: ---> 重复输入新的 su 密码  
这样你的 su 的密码设置好了。  
注：命令为passwd而不是password  
2. 在terminal中利用su命令就可以切换到root用户了。  
注：su和sudo的区别是：  
1). su的密码是root的密码，而sudo的密码是用户的密码；  
2). su直接将身份变成root，而sudo是以用户登录后以root的身份运行命令，不需要知道root密码；  