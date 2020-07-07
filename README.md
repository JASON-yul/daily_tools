# #!/usr/bin/expect
set timeout 3
set package ***-1.0-RELEASE #定义变量

#spawn scp root@ip:/mnt/jenkins/*/*/*/target/$package.jar /mnt/  #交互式传输，不适合流水线
sshpass -p JASONyl123 scp root@10.28.10.78:/mnt/jenkins/*/*/*/target/$package.jar  /mnt/ #直接传输，可用在流水线上
#expect "*password:*"
#send "password\r"
#interact
