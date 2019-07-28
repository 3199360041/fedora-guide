xcode-select --install

安装iTerm2

/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

brew tap homebrew/cask

cd "$(brew --repo)"
git remote set-url origin https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/brew.git

cd "$(brew --repo)/Library/Taps/homebrew/homebrew-core"
git remote set-url origin https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/homebrew-core.git

cd "$(brew --repo)"/Library/Taps/homebrew/homebrew-cask
git remote set-url origin https://mirrors.ustc.edu.cn/homebrew-cask.git



bash（默认 shell）用户：

echo 'export HOMEBREW_BOTTLE_DOMAIN=https://mirrors.ustc.edu.cn/homebrew-bottles' >> ~/.bash_profile
source ~/.bash_profile


zsh 用户：

echo 'export HOMEBREW_BOTTLE_DOMAIN=https://mirrors.ustc.edu.cn/homebrew-bottles' >> ~/.zshrc
source ~/.zshrc


brew update

brew install zsh

sudo chsh -s /usr/local/bin/zsh

安装Oh My ZSH
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

brew install wget
brew install git-flow


brew cask install visual-studio-code
brew cask install google-chrome

brew install python@3

vim ~/.pip/pip.conf

[global]
index-url=https://pypi.tuna.tsinghua.edu.cn/simple


brew install php@7.3
brew link php@7.3

终端中输入

    brew search php
    brew install php@7.3
    brew link php@7.3

brew link 出现warning执行（使用zsh的可将bash_profile改为zshrc）

   echo 'export PATH="/usr/local/opt/php@7.3/bin:$PATH"' >> ~/.bash_profile
   echo 'export PATH="/usr/local/opt/php@7.3/sbin:$PATH"' >> ~/.bash_profile



   安装nginx
可以用brew很方便地安装nginx.    
sudo brew install nginx
启动nginx服务 
sudo brew services start nginx
利用http://localhost:8080进行访问, 说明启动成功.



brew install composer

composer config -g repo.packagist composer https://mirrors.aliyun.com/composer/
