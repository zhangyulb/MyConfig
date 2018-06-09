## Basics
All Docs, Medias, backuped on OneDrive  
Must-be-ready tools: Office365, Cmder-Mini, Ubuntu Linux Subsystem

## For Linux Subsystem
### 1. Edit software source
cd /etc/apt && mv sources.list sources.list.bak  
wget http://mirrors.163.com/.help/sources.list.lucid  
mv sources.list.lucid sources.list  
apt-get update  
apt-get dist-upgrade  
