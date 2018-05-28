### 安装 YouCompleteMe
```
sudo dnf install automake gcc gcc-c++ kernel-devel cmake

sudo dnf install python-devel python3-devel

cd ~/.vim/bundle

git clone https://github.com/Valloric/YouCompleteMe.git 

cd YouCompleteMe

git submodule update --init --recursive

./install.py --clang-completer --go-completer --js-completer

```