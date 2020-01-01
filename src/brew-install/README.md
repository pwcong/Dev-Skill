# Install HomeBrew

官网地址[HomeBrew](https://brew.sh/)

#### 0x01
下载安装脚本

```shell
curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install >> brew_install
```

修改安装脚本
```shell
vim brew_install

# 找到BREW_REPO变量并替换，修改后如下：
BREW_REPO = "git://mirrors.ustc.edu.cn/brew.git".freeze

```

开始安装
```shell
ruby brew_install
```

#### 0x02
修改包安装源

```shell
cd "$(brew --repo)"
 
git remote set-url origin https://mirrors.aliyun.com/homebrew/brew.git
 
cd "$(brew --repo)/Library/Taps/homebrew/homebrew-core"
 
git remote set-url origin https://mirrors.aliyun.com/homebrew/homebrew-core.git
 
echo 'export HOMEBREW_BOTTLE_DOMAIN=https://mirrors.aliyun.com/homebrew/homebrew-bottles' >> ~/.bash_profile

source ~/.bash_profile

```

更新并检查

```shell
brew update

brew doctor
```
