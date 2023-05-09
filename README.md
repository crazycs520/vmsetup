# vmsetup

```shell
sudo yum install zsh git tmux htop -y

mkdir -p ./code/goread

sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-completions ${ZSH_CUSTOM:=~/.oh-my-zsh/custom}/plugins/zsh-completions
```


zshrc

```shell
export GO111MODULE=on
export GOPATH=$HOME/code/goread
export GOROOT=/usr/local/go
export GOBIN=$GOPATH/bin
export PATH=$GOBIN:$GOROOT/bin:$PATH

plugins=(sudo colored-man-pages  git history zsh-autosuggestions zsh-completions zsh-syntax-highlighting)

source ~/.alias
```