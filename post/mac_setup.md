```shell
xcode-select --install

/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

brew tap homebrew/cask

cd "$(brew --repo)"

git remote set-url origin https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/brew.git

cd "$(brew --repo)/Library/Taps/homebrew/homebrew-core"

git remote set-url origin https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/homebrew-core.git

cd "$(brew --repo)"/Library/Taps/homebrew/homebrew-cask

git remote set-url origin https://mirrors.ustc.edu.cn/homebrew-cask.git
```
###   bash（默认 shell）用户：
```shell
echo 'export HOMEBREW_BOTTLE_DOMAIN=https://mirrors.ustc.edu.cn/homebrew-bottles' >> ~/.bash_profile

source ~/.bash_profile
```

###   zsh 用户：
```shell
echo 'export HOMEBREW_BOTTLE_DOMAIN=https://mirrors.ustc.edu.cn/homebrew-bottles' >> ~/.zshrc

source ~/.zshrc

brew update

brew install zsh

cat /etc/shells

sudo su

#echo "/usr/local/bin/zsh" >> /etc/shells

sudo chsh -s /usr/local/bin/zsh
```

###   安装Oh My ZSH
```shell
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

brew install wget

brew install git-flow

brew cask install visual-studio-code

brew cask install google-chrome
```
### 安装iTerm2
[iTerm2](https://iterm2.com)

###   安装python3
```shell
brew install python@3

vim ~/.pip/pip.conf

[global]
index-url=https://pypi.tuna.tsinghua.edu.cn/simple
```
###   安装php7.3
```shell
brew search php

brew install php@7.3

brew link php@7.3
```

### brew link 出现warning执行（使用zsh的可将bash_profile改为zshrc）
```shell
   echo 'export PATH="/usr/local/opt/php@7.3/bin:$PATH"' >> ~/.bash_profile
   echo 'export PATH="/usr/local/opt/php@7.3/sbin:$PATH"' >> ~/.bash_profile
```

###   安装composer
```shell
brew install composer

composer config -g repo.packagist composer https://mirrors.aliyun.com/composer/
```
###   安装nginx
```shell
brew instal nginx  

sudo brew services start nginx

curl -I http://localhost:8080/

```
