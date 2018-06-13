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

### 2. Install desktop (for Linux subsystem of Windows OS)
1. Install X-Windows for Windows OS: [a link](https://sourceforge.net/projects/vcxsrv/)  
2. Launch XLaunch, set “One large window" mode, and Display number = 0. Leave other configs as default.
3. Install ubuntu desktop in the Linux subsystem: `sudo apt-get install ubuntu-desktop unity compizconfig-settings-manager`. NOTE: if this step fails at installing the ppp package due to the unavailability of gdm service, edit the script in /etc/init.d/pppd-dns and delete "gdm" from Required-Start.
4. Configure the compiz manager: `echo DISPLAY=localhost:0 >> ~/.bashrc && source ~/.bashrc`, and run "ccsm" in Linux subsystem. Check "Ubuntu unity plugin" and leave other options as default.
5. Close ccsm and run "compiz" in the Linux subsystem.

### Install useful packages
`apt-get install aptitude`  
`aptitude install python2.7 python-pip python-dev python3-dev libncurses5-dev build-essential`

## Configure github
Cloning from github has been slow in China. Add the following IP addresses into host:  
`151.101.72.249 http://global-ssl.fastly.Net`  
`192.30.253.112 http://github.com`  

### Install VIM
Refer to [My VIM Settings](https://github.com/zhangyulb/python-vim/README.md)
