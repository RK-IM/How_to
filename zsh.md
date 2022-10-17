# zsh 설치
```
sudo apt install zsh
chsh -s $(which zsh)

# 재부팅 후 쉘 실행
# 기본 쉘 적용 확인
ehco $SHELL

# Oh My Zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```
# zsh 설정
```
# 테마 설정
gedit ~/.zshrc
ZSH_THEME 수정

# 폰트 설정
sudo apt install fonts-powerline

# 플러그인 sudo, colored-man-pages, zsh-syntax-highlighting, zsh-autosuggestions, fzf

# zsh-syntax-highlighting

git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
# zsh-autosuggestions

git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
# fzf (Fuzzy Finder)

git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf
~/.fzf/install

# 플러그인 사용
gedit ~/.zshrc
plugins = (git
sudo
colored-man-pages
zsh-syntax-highlighting
zsh-autosuggestions
fzf
)

# 적용
source ~/.zshrc
```
# zsh에서 conda 실행 안될 때
```
gedit ~/.zshrc

# User Configuration 아래에 다음 추가
export PATH=~/anaconda3/bin:$PATH

source ~/.zshrc
```
