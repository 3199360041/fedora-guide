  ### 移除libreoffice, 安装vim、gnome-terminal-nautilus及C开发套件，设置自动登录 
```
  sudo dnf remove libreoffice-draw libreoffice-graphicfilter libreoffice-impress libreoffice-writer libreoffice-pyuno libreoffice-math libreoffice-calc libreoffice-emailmerge 

  sudo dnf install gnome-terminal-nautilus

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

设置自动登录
```
vim /etc/gdm/custom.conf

[daemon]
AutomaticLoginEnable=True
AutomaticLogin=pzzrudlf

```
