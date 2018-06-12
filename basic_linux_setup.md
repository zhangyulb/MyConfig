### 1. Edit software source
`cd /etc/apt && cp sources.list sources.list.bak`  
Remove all the content in sources.list and paste the following text into it:  
deb http://mirrors.163.com/ubuntu/ xenial main restricted universe multiverse  
deb http://mirrors.163.com/ubuntu/ xenial-security main restricted universe multiverse  
deb http://mirrors.163.com/ubuntu/ xenial-updates main restricted universe multiverse  
deb http://mirrors.163.com/ubuntu/ xenial-proposed main restricted universe multiverse  
deb http://mirrors.163.com/ubuntu/ xenial-backports main restricted universe multiverse  
deb-src http://mirrors.163.com/ubuntu/ xenial main restricted universe multiverse  
deb-src http://mirrors.163.com/ubuntu/ xenial-security main restricted universe multiverse  
deb-src http://mirrors.163.com/ubuntu/ xenial-updates main restricted universe multiverse  
deb-src http://mirrors.163.com/ubuntu/ xenial-proposed main restricted universe multiverse  
deb-src http://mirrors.163.com/ubuntu/ xenial-backports main restricted universe multiverse  
`apt-get update`  

### Install packages
`apt-get install aptitude`  
`aptitude install python-pip python-dev build-essential`

### Install Vim
Refer to [Vim for Python](https://github.com/zhangyulb/python-vim/README.md)
