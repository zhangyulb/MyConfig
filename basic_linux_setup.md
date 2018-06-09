### 1. Edit software source
`cd /etc/apt && cp sources.list sources.list.bak`  
Remove all the content in sources.list and paste the following text into it:  
deb http://mirrors.aliyun.com/ubuntu/ trusty main restricted universe multiverse  
deb http://mirrors.aliyun.com/ubuntu/ trusty-security main restricted universe multiverse  
deb http://mirrors.aliyun.com/ubuntu/ trusty-updates main restricted universe multiverse  
deb http://mirrors.aliyun.com/ubuntu/ trusty-proposed main restricted universe multiverse  
deb http://mirrors.aliyun.com/ubuntu/ trusty-backports main restricted universe multiverse  
deb-src http://mirrors.aliyun.com/ubuntu/ trusty main restricted universe multiverse  
deb-src http://mirrors.aliyun.com/ubuntu/ trusty-security main restricted universe multiverse  
deb-src http://mirrors.aliyun.com/ubuntu/ trusty-updates main restricted universe multiverse  
deb-src http://mirrors.aliyun.com/ubuntu/ trusty-proposed main restricted universe multiverse  
deb-src http://mirrors.aliyun.com/ubuntu/ trusty-backports main restricted universe multiverse  
`apt-get update && apt-get dist-upgrade`  

### Install packages
`apt-get install python2.7`
