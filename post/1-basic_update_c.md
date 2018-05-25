  ### 更新系统及安装vim及C开发套件 ###
```
  sudo dnf update -y
  sudo dnf install vim -y
  sudo dnf groupinstall 'C Development Tools and Libraries' -y
```
格式化c代码命令
```
#!/bin/bash
indent -kr -i8 -ts8 -sob -l80 -ss -bs -psl $1
```
保存为cid.sh文件，然后执行如下命令
```
sudo cp cid.sh /usr/local/bin/cid
```
