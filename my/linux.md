---
title: Linux
layout: upj_design
permalink: /linux/
---

#### Table Of Contents

- TOC
{:toc}

# Linux
{: #upj_1676507688026}

Linux 활용법

## Install
{: #upj_1676507693577}

- Windows Subsystem for Linux
  - [WSL](https://learn.microsoft.com/ko-kr/windows/wsl/install)
- Cloud Service
  - [Oracle](https://www.oracle.com/cloud/)
  - [Google](https://cloud.google.com/?hl=ko)
  - [Amazon](https://aws.amazon.com/ko/)
  - [Microsoft](https://azure.microsoft.com/ko-kr/)
  - [Naver](https://www.ncloud.com/)
- Virtual Machine
  - [Oracle VirtualBox](https://www.virtualbox.org/)
  - [VM Ware](https://www.vmware.com/kr.html)

## 기본 명령어
{: #upj_1676507701281}

### 파일 관련 명령어
{: #upj_1676507714361}

파일 보기: ls

```shell
ls -l 	long list
ls -a		all
ls -al	all + long
ls *.txt	확장자 txt만 보기
```

파일 내용 보기

```shell
cat  hello.txt	
cat -e hello.txt	줄의 맨 뒤에 $붙이기
cat -n hello.txt	줄 번호 보여주기
more  hello.txt	페이지 단위로 보기
less  hello.txt	more보다 향상된 기능
```

파일 만들기/지우기

```shell
touch  hello.txt	파일 만들기
rm  hello.txt		파일 삭제
rm -r hello		디렉토리 삭제
rm -f hello.txt	강제 삭제
rm -rf hello		디렉토리 + 강제
```

파일 복사

```shell
cp  hello.txt  dir1
```

파일 이동

```shell
mv  hello.txt  dir2
mv  hello1.txt  hello2.txt	파일 이름 변경
```

파일 숏컷

```shell
ln -s hello.txt hellosym	소프트링크(심볼릭)
ln hello.txt hellolink		하드링크
ls -ali	파일 링크 확인
```

파일 속성 보기

```shell
file hello.txt
```

### 디렉토리 관련 명령어
{: #upj_1676507724193}

디렉토리 만들기

```shell
mkdir dir1
```

디렉토리 이동

```shell
cd ~	홈 디렉토리
cd ..		부모 디렉토리
cd -		이전 디렉토리
pwd		현재 디렉토리 확인
clear 터미널 지우기
```

### 시스템 및 기타 유용한 명령어
{: #upj_1676507729273}

시스템 종료

```shell
reboot	재부팅
poweroff	종료
shutdown -P now	바로 종료
shutdown -r now	바로 재시작
shutdown -h +10	10분 후 종료
shutdown -r 21:00	오후9시에 재부팅
```

```text
ssh 파일 업로드 하기
scp ./Raspberry_Pi.png upj53@192.168.0.2:/home/upj53/webapp/static
```

### 용량 부족할 때 파일 지우기
{: #upj_1705714728906}

```bash
# 폴더 용량 확인
df -h

# 휴지통 비우기
rm -rf ~/.local/share/Trash/files/*

# 크기 별로 정렬해서 보기
ls -alhS

# 파일 및 폴더 크기 보기
du -ah *

# 특정 폴더의 용량 합계
du -sh /folder

# 특정 경로에 있는 모든 폴더 별로 용량 합계
du -h -d 1

# 패턴으로 파일/폴더 삭제
find /folder -name '*.log' #-delete
```

## 사용자와 그룹 및 권한 관리
{: #upj_1676507738746}

### 권한 확인
{: #upj_1676507743433}

계정 권한 확인/권한 대여

```shell
whoami	내가 누구인지 내 계정 확인
id		내가 갖고 있는 권한 확인

cat /etc/passwd	사용자 계정 확인
cat /etc/shadow	사용자 암호
cat /etc/group	사용자 그룹 확인
passwd user1	암호 재설정

sudo	슈퍼유저의 권한을 수행(do)한다
```

### 사용자 그룹 추가 삭제
{: #upj_1676507749993}

사용자 추가

```shell
     사용자 추가
sudo useradd user1

     사용자를 sudo 권한에 추가

useradd -aG sudo user1 # 우분투

     사용자 삭제
sudo deluser user1
sudo deluser user1 --remove-home
```

그룹 추가

```shell
     그룹 생성/삭제
sudo addgroup dev
sudo delgroup dev

     그룹에 사용자 할당
sudo usermod -aG sudo user1
```

### 파일시스템 권한
{: #upj_1676507757409}

권한 정보

<table class="post">
<thead>
<tr>
  <th colspan="3">소유자(Owner)</th>
  <th colspan="3">그룹(Group)</th>
  <th colspan="3">그외(Other)</th>
</tr>
</thead>
<tbody>
<tr>
  <td>읽기</td><td>쓰기</td><td>실행</td>
  <td>읽기</td><td>쓰기</td><td>실행</td>
  <td>읽기</td><td>쓰기</td><td>실행</td>
</tr>
<tr>
  <td>r</td><td>w</td><td>x</td>
  <td>r</td><td>w</td><td>x</td>
  <td>r</td><td>w</td><td>x</td>
</tr>
<tr>
  <td>4</td><td>2</td><td>1</td>
  <td>4</td><td>2</td><td>1</td>
  <td>4</td><td>2</td><td>1</td>
</tr>
</tbody>
</table>

권한/소유권 변경

```shell
권한 변경
chmod 777 hello.txt
chmod 700 hello.txt
chmod u+x hello.txt
chmod g-rx hello.txt
chmod o-x hello.txt
chmod +rwx hello.txt

소유권 변경
chown user2 hello.txt		소유자 변경
chown user2:user2 hello.txt	소유자+그룹 변경
chown :user2 hello.txt		그룹 변경
```

## Bash 쉘 다루기
{: #upj_1676507764514}

### 환경변수 PATH
{: #upj_1676507769743}

```shell
echo $PATH
export PATH=$PATH:추가할디렉토리

     프롬프트 스타일 변경
echo $PS1
PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\]\n> '
```

### 기본 문법
{: #upj_1676507775481}

```shell
     모든 쉘 확인
cat /etc/shells

     나의 쉘 확인
echo $0
echo $SHELL

     명령어 히스토리: history
history 10	최근 10개 히스토리 보기
history -c	히스토리 버퍼 삭제
!15		15번째 명령어 실행
!!		바로 이전 명령어 실행

     명령어 실행 위치 파악
which ls
which python

     단축 명령어
alias 단축 명령어 확인
alias ..=”cd ..”
alias …=”cd ../..

     쉘 부팅(시작) 시퀀스
.profile
.bashrc  .bash_history  .bash_logout
```

### 입출력
{: #upj_1676507781609}

```shell
결과물을 다른 장치로 보냄
ls > file.txt		출력 결과물을 파일로 출력
ls >> file.txt		기존 파일에 누적
aaa 2> file.txt	실패한 결과물을 출력

파이프: 출력값 프로세스간 전달
ls -l | grep hello	출력값 내에서 검색
ls -l | wc -l		줄 개수 확인
ls -l | grep hello | wc -l	다중 파이프 처리
cat hello.txt | more	출력값 페이징 처리
```

### bashrc 샘플
{: #upj_1676507786473}

2024-04-17 renewal

```shell
# ~/.bashrc: executed by bash(1) for non-login shells.
# see /usr/share/doc/bash/examples/startup-files (in the package bash-doc)
# for examples

# If not running interactively, don't do anything
[ -z "$PS1" ] && return

# don't put duplicate lines in the history. See bash(1) for more options
# ... or force ignoredups and ignorespace
HISTCONTROL=ignoredups:ignorespace

# append to the history file, don't overwrite it
shopt -s histappend

# for setting history length see HISTSIZE and HISTFILESIZE in bash(1)
HISTSIZE=1000
HISTFILESIZE=2000

# check the window size after each command and, if necessary,
# update the values of LINES and COLUMNS.
shopt -s checkwinsize

# make less more friendly for non-text input files, see lesspipe(1)
[ -x /usr/bin/lesspipe ] && eval "$(SHELL=/bin/sh lesspipe)"

# set variable identifying the chroot you work in (used in the prompt below)
if [ -z "$debian_chroot" ] && [ -r /etc/debian_chroot ]; then
    debian_chroot=$(cat /etc/debian_chroot)
fi

# set a fancy prompt (non-color, unless we know we "want" color)
case "$TERM" in
    xterm-color) color_prompt=yes;;
esac

# uncomment for a colored prompt, if the terminal has the capability; turned
# off by default to not distract the user: the focus in a terminal window
# should be on the output of commands, not on the prompt
force_color_prompt=yes

if [ -n "$force_color_prompt" ]; then
    if [ -x /usr/bin/tput ] && tput setaf 1 >&/dev/null; then
	# We have color support; assume it's compliant with Ecma-48
	# (ISO/IEC-6429). (Lack of such support is extremely rare, and such
	# a case would tend to support setf rather than setaf.)
	color_prompt=yes
    else
	color_prompt=
    fi
fi

if [ "$color_prompt" = yes ]; then
    PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\]\n> '
else
    PS1='${debian_chroot:+($debian_chroot)}\u@\h:\w\$ '
fi
unset color_prompt force_color_prompt

# If this is an xterm set the title to user@host:dir
case "$TERM" in
xterm*|rxvt*)
    PS1="\[\e]0;${debian_chroot:+($debian_chroot)}\u@\h: \w\a\]$PS1"
    ;;
*)
    ;;
esac

# enable color support of ls and also add handy aliases
if [ -x /usr/bin/dircolors ]; then
    test -r ~/.dircolors && eval "$(dircolors -b ~/.dircolors)" || eval "$(dircolors -b)"
    alias ls='ls --color=auto'
    #alias dir='dir --color=auto'
    #alias vdir='vdir --color=auto'

    alias grep='grep --color=auto'
    alias fgrep='fgrep --color=auto'
    alias egrep='egrep --color=auto'
fi

# Alias definitions.
# You may want to put all your additions into a separate file like
# ~/.bash_aliases, instead of adding them here directly.
# See /usr/share/doc/bash-doc/examples in the bash-doc package.

if [ -f ~/.bash_aliases ]; then
    . ~/.bash_aliases
fi

# enable programmable completion features (you don't need to enable
# this, if it's already enabled in /etc/bash.bashrc and /etc/profile
# sources /etc/bash.bashrc).
#if [ -f /etc/bash_completion ] && ! shopt -oq posix; then
#    . /etc/bash_completion
#fi

# >>> conda initialize >>>
# !! Contents within this block are managed by 'conda init' !!
__conda_setup="$('/opt/miniconda3/bin/conda' 'shell.bash' 'hook' 2> /dev/null)"
if [ $? -eq 0 ]; then
    eval "$__conda_setup"
else
    if [ -f "/opt/miniconda3/etc/profile.d/conda.sh" ]; then
        . "/opt/miniconda3/etc/profile.d/conda.sh"
    else
        export PATH="/opt/miniconda3/bin:$PATH"
    fi
fi
unset __conda_setup
# <<< conda initialize <<<

# Install Ruby Gems to ~/gems
export GEM_HOME="$HOME/gems"
export PATH="$HOME/gems/bin:$PATH"

# My Path
conda activate py310

export PATH="$HOME/.local/bin:$PATH"

. "$HOME/.cargo/env"

export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion

# git setting
parse_git_branch()
{
    git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/(\1)/'
}
c_cyan=`tput setaf 6`
c_red=`tput setaf 1`
c_green=`tput setaf 2`
c_sgr0=`tput sgr0`
branch_color ()
{
   if git rev-parse --git-dir >/dev/null 2>&1
   then
      color=""
      if git diff --quiet 2>/dev/null >&2
      then
         color="${c_green}"
      else
         color=${c_red}
      fi
   else
      return 0
   fi
   echo -ne $color
}

#export PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\]\n> '
export PS1='\e[01;32m\u@\h \[\e[34m\]\w \[${c_sgr0}\]\[$(branch_color)\]$(parse_git_branch)\[${c_sgr0}\]\n> '

cd "/workspace/GITHUB-IO"
git pull
git fetch
clear
```

old version

```shell
# ~/.bashrc: executed by bash(1) for non-login shells.
# see /usr/share/doc/bash/examples/startup-files (in the package bash-doc)
# for examples

# If not running interactively, don't do anything
case $- in
    *i*) ;;
      *) return;;
esac

# don't put duplicate lines or lines starting with space in the history.
# See bash(1) for more options
HISTCONTROL=ignoreboth

# append to the history file, don't overwrite it
shopt -s histappend

# for setting history length see HISTSIZE and HISTFILESIZE in bash(1)
HISTSIZE=1000
HISTFILESIZE=2000

# check the window size after each command and, if necessary,
# update the values of LINES and COLUMNS.
shopt -s checkwinsize

# If set, the pattern "**" used in a pathname expansion context will
# match all files and zero or more directories and subdirectories.
#shopt -s globstar

# make less more friendly for non-text input files, see lesspipe(1)
[ -x /usr/bin/lesspipe ] && eval "$(SHELL=/bin/sh lesspipe)"

# set variable identifying the chroot you work in (used in the prompt below)
if [ -z "${debian_chroot:-}" ] && [ -r /etc/debian_chroot ]; then
    debian_chroot=$(cat /etc/debian_chroot)
fi

# set a fancy prompt (non-color, unless we know we "want" color)
case "$TERM" in
    xterm-color|*-256color) color_prompt=yes;;
esac

# uncomment for a colored prompt, if the terminal has the capability; turned
# off by default to not distract the user: the focus in a terminal window
# should be on the output of commands, not on the prompt
#force_color_prompt=yes

if [ -n "$force_color_prompt" ]; then
    if [ -x /usr/bin/tput ] && tput setaf 1 >&/dev/null; then
	# We have color support; assume it's compliant with Ecma-48
	# (ISO/IEC-6429). (Lack of such support is extremely rare, and such
	# a case would tend to support setf rather than setaf.)
	color_prompt=yes
    else
	color_prompt=
    fi
fi

if [ "$color_prompt" = yes ]; then
    PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\]\n> '
else
    PS1='${debian_chroot:+($debian_chroot)}\u@\h:\w\$ '
fi
unset color_prompt force_color_prompt

# If this is an xterm set the title to user@host:dir
case "$TERM" in
xterm*|rxvt*)
    PS1="\[\e]0;${debian_chroot:+($debian_chroot)}\u@\h: \w\a\]$PS1"
    ;;
*)
    ;;
esac

# enable color support of ls and also add handy aliases
if [ -x /usr/bin/dircolors ]; then
    test -r ~/.dircolors && eval "$(dircolors -b ~/.dircolors)" || eval "$(dircolors -b)"
    alias ls='ls --color=auto'
    #alias dir='dir --color=auto'
    #alias vdir='vdir --color=auto'

    alias grep='grep --color=auto'
    alias fgrep='fgrep --color=auto'
    alias egrep='egrep --color=auto'
fi

# colored GCC warnings and errors
#export GCC_COLORS='error=01;31:warning=01;35:note=01;36:caret=01;32:locus=01:quote=01'

# Add an "alert" alias for long running commands.  Use like so:
#   sleep 10; alert
alias alert='notify-send --urgency=low -i "$([ $? = 0 ] && echo terminal || echo error)" "$(history|tail -n1|sed -e '\''s/^\s*[0-9]\+\s*//;s/[;&|]\s*alert$//'\'')"'

# Alias definitions.
# You may want to put all your additions into a separate file like
# ~/.bash_aliases, instead of adding them here directly.
# See /usr/share/doc/bash-doc/examples in the bash-doc package.

if [ -f ~/.bash_aliases ]; then
    . ~/.bash_aliases
fi

alias l='ls -lt'
alias la='ls -alt'
alias c='clear'
alias ..='cd ..'
alias ...='cd ../../'

# enable programmable completion features (you don't need to enable
# this, if it's already enabled in /etc/bash.bashrc and /etc/profile
# sources /etc/bash.bashrc).
if ! shopt -oq posix; then
  if [ -f /usr/share/bash-completion/bash_completion ]; then
    . /usr/share/bash-completion/bash_completion
  elif [ -f /etc/bash_completion ]; then
    . /etc/bash_completion
  fi
fi

# tomcat & java
CATALINA_HOME="/opt/tomcat/apache-tomcat-8.5.65"
JAVA_HOME="/usr/lib/jvm/java-8-openjdk-amd64"
export PATH="$PATH:$JAVA_HOME/bin:$CATALINA_HOME\bin"
export CATALINA_HOME
export JAVA_HOME

export NLS_LANG=KOREAN_KOREA.AL32UTF8
```

## Zsh 쉘 다루기
{: #upj_1676507803753}

### Oh My Zsh
{: #upj_1676507807745}

```shell
sudo apt install zsh -y
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

[oh-my-zsh](https://ohmyz.sh/)

### PowerLevel10k
{: #upj_1676507813314}

```shell
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

Font Family: MesloLGS NF

```json
{
  "profiles": {
    "defaults": {
      "fontFace": "MesloLGS NF"
    }
  }
}
```

[Powerlevel10k](https://github.com/romkatv/powerlevel10k)

## Vim Editor
{: #upj_1676507819857}

<a href="https://kldp.org/files/vi-vim-cheat-sheet-ko.png" target="_blank">
<img src="/assets/images/vim-shortkey.png" style="width: 75%; height:auto; "/>
</a>

- [Vim Editor Official](https://www.vim.org/)
- [Vim Genius](http://vimgenius.com/)
- [Open Vim](https://openvim.com/)
- [Vim Adventures](https://vim-adventures.com/)
- [Learn Vim Progressively](https://yannesposito.com/Scratch/en/blog/Learn-Vim-Progressively/)
- [Learning Vim in 2014](https://benmccormick.org/learning-vim-in-2014/)
- [VIM Casts](http://vimcasts.org/)
- [Vim Videos](http://derekwyatt.org/vim/tutorials/)
- [Learn Vimscript the Hard Way](https://learnvimscriptthehardway.stevelosh.com/)
- [Seven habits of effective text editing](https://www.moolenaar.net/habits.html)
- [VIM-Galore](https://github.com/mhinz/vim-galore)

### vim 유용한 단축키
{: #upj_1676634356913}

```text
:vsp 세로로 창 쪼개서 열기
:sp 가로로 창 쪼개서 열기

창 너비 width 조절
Ctl+w → 30>
Ctl+w → 10<

창 높이 height 조절
Ctl+w → 30+
Ctl+w → 10-

창 너비 width 최대로
Ctl+w → |
창 높이 height 최대로
Ctl+w → _
창 높이 똑같이
Ctl+w → =
```

### Vim as your editor
{: #upj_1705714728849}

```text
Command   Count   
	d
	c
	y
	v
```

화면 한페이지씩 이동 후 정중앙에 놓기

```vim
nnoremap("<C-d>", "<C-d>zz")
nnoremap("<C-u>", "<C-u>zz")

상대적인 줄번호 켜기

" turn relative line numbers on
:set relativenumber
:set rnu

" turn relative line numbers off
:set norelativenumber
:set nornu

" toggle relative line numbers
:set relativenumber!
:set rnu!

nnoremap("n", "nzzzv")
nnoremap("N", "Nzzzv")

xnoremap("<leader>p", "\"_dP")
```

### vimrc 샘플
{: #upj_1676507797625}

[Vim Cursor and Tip](https://frhyme.github.io/vim/vim08_cursorline),
[jellybeans scheme](https://github.com/nanotech/jellybeans.vim),
[NERDTree](https://github.com/preservim/nerdtree),
[작업 효율을 높여주는 Plugins](https://www.youtube.com/watch?v=ONcFKXoJ7uQ),
[Python vim setting](https://linuxhint.com/vim-python-development/),
[Python 인덴트 구분자](https://kwonnam.pe.kr/wiki/vim/indent)

NerdTree 설치하기

```bash
git clone https://github.com/preservim/nerdtree.git ~/.vim/pack/vendor/start/nerdtree
vim -u NONE -c "helptags ~/.vim/pack/vendor/start/nerdtree/doc" -c q
```

Python vim

```bash
wget https://raw.githubusercontent.com/hdima/python-syntax/master/syntax/python.vim
```

리뉴얼

```vim
colorscheme torte
"colorscheme slate

"set autoindent "불필요
"set softtabstop=4 "불필요

set number "set nu! 줄번호
set relativenumber "set rnu! 는 relativenumber토글
set tabstop=4
set shiftwidth=4
set smarttab
set smartindent
set mouse=a "마우스로 스크롤 및 리사이즈 가능. [n : Normal mode / v : Visual mode / i : Insert mode / a : All modes]
set nocompatible "오리지날 VI와 호환하지 않음
set laststatus=2 "상태바 표시. (= ls) [0: 상태바 미표시 / 1: 2개 이상의 윈도우에서 표시 / 2: 항상 표시]
set backspace=indent,eol,start "백스페이스가 작동한다
set ruler
set noundofile
set nobackup
set nowritebackup
set noswapfile
set showmatch
set hlsearch
set encoding=utf-8
set fileencodings=utf8,cp949,euc-kr
set autowrite
set autowriteall
set splitbelow
set splitright
syntax enable
"set clipboard=unnamed
set clipboard=unnamedplus
set cursorline "커서가 있는 라인을 강조 표시.
set nowrapscan "검색할 때 문서의 끝에서 처음으로 안돌아감
set tenc=utf-8 "터미널 인코딩
set history=1000 "vi 편집기록 기억갯수 .viminfo에 기록
"set expandtab " 탭대신 스페이스

"Vundle Plugin 세팅
"https://github.com/VundleVim/Vundle.vim
" 설치
" git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
" 플러그인 모두 설치
" vim +PluginInstall +qall
filetype off "required

" set the runtime path to include Vundle and initialize
set rtp+=~/.vim/bundle/Vundle.vim
call vundle#begin()
" alternatively, pass a path where Vundle should install plugins
"call vundle#begin('~/some/path/here')

" let Vundle manage Vundle, required
Plugin 'VundleVim/Vundle.vim'

" The following are examples of different formats supported.
" Keep Plugin commands between vundle#begin/end.
" plugin on GitHub repo
Plugin 'tpope/vim-fugitive'
" plugin from http://vim-scripts.org/vim/scripts.html
" Plugin 'L9'
" Git plugin not hosted on GitHub
Plugin 'git://git.wincent.com/command-t.git'
" git repos on your local machine (i.e. when working on your own plugin)
" Plugin 'file:///home/gmarik/path/to/plugin'
" The sparkup vim script is in a subdirectory of this repo called vim.
" Pass the path to set the runtimepath properly.
Plugin 'rstacruz/sparkup', {'rtp': 'vim/'}
" Install L9 and avoid a Naming conflict if you've already installed a
" different version somewhere else.
" Plugin 'ascenator/L9', {'name': 'newL9'}

" All of your Plugins must be added before the following line

" vim-airline
" https://github.com/vim-airline/vim-airline?tab=readme-ov-file
Plugin 'vim-airline/vim-airline'
" Plugin 'vim-airline/vim-airline-themes'
let g:airline#extensions#tabline#enabled = 1              " vim-airline 버퍼 목록 켜기
let g:airline#extensions#tabline#fnamemod = ':t'          " vim-airline 버퍼 목록 파일명만 출력
let g:airline#extensions#tabline#buffer_nr_show = 1       " buffer number를 보여준다
let g:airline#extensions#tabline#buffer_nr_format = '%s:' " buffer number format

" TagBar
" sudo apt install universal-ctags
Plugin 'majutsushi/tagbar'
" F12 를 tagbar 토글 키로 사용
"map <F12> :TagbarToggle<CR>
" tagbar 가로 사이즈 설정
"let g:tagbar_width=40

call vundle#end()            " required
filetype plugin indent on    " required
" To ignore plugin indent changes, instead use:
"filetype plugin on
"
" Brief help
" :PluginList       - lists configured plugins
" :PluginInstall    - installs plugins; append `!` to update or just :PluginUpdate
" :PluginSearch foo - searches for foo; append `!` to refresh local cache
" :PluginClean      - confirms removal of unused plugins; append `!` to auto-approve removal
"
" see :h vundle for more details or wiki for FAQ
" Put your non-Plugin stuff after this line

" 단축키
"Vertical, Horizental 창크기+3-3
nnoremap <C-A-Right> :vert resize +3<CR>
nnoremap <C-A-Left> :vert resize -3<CR>
nnoremap <C-A-Up> :resize +3<CR>
nnoremap <C-A-Down> :resize -3<CR>

"Vertial 창열기
nnoremap <C-A-PageDown> :vs %:p<CR>
"Horizental 창열기
nnoremap <C-A-PageUp> :sp %:p<CR>
"창닫기 :q
"nnoremap <C-q> :quit<CR>
"모든창닫기 :wqa!

nnoremap <C-o> :NERDTreeToggle<CR>
let g:NERDTreeWinSize=20

nnoremap <C-t> :terminal<CR>

"이전 버퍼로 이동
nnoremap <C-h> :bprevious!<Enter>
"다음 버퍼로 이동
nnoremap <C-l> :bnext!<Enter>
"현재 버퍼를 닫고 이전 버퍼로 이동
nnoremap <C-j> :bp <BAR> bd #<Enter>
```

```vim
옛날 버전
source ~/.vim_config

"nnoremap <leader>n :NERDTreeFocus<CR>
"nnoremap <C-n> :NERDTree<CR>
"nnoremap <C-f> :NERDTreeFind<CR>
nnoremap <C-o> :NERDTreeToggle<CR>
nnoremap <C-t> :terminal<CR>

"colorscheme jellybeans
colorscheme torte

set nocp
set number
set ts=2 sw=2 et
set sts=2
set laststatus=2
set smarttab
set smartindent
set softtabstop=2
set backspace=indent,eol,start
set ruler
autocmd InsertEnter * set cul
autocmd InsertLeave * set nocul
let &t_SI = "\<ESC>[6 q"
let &t_EI = "\<ESC>[2 q"
set noundofile
set nobackup
set nowritebackup
set noswapfile
set showmatch
set hlsearch
set noundofile
set nobackup
set nowritebackup
set noswapfile
set fileencodings=utf8,euc-kr
set autowrite
set autowriteall
set splitbelow
set splitright
syntax enable
let python_highlight_all = 1

set guifont=Bitstream_Vera_Sans_Mono:h27:cHANGEUL
```

## NeoVim Editor
{: #upj_1705714728909}

### install
{: #upj_1705714728908}

- [LunarVim 설치](https://www.lunarvim.org/docs/installation)
- [Download Neovim AppImage](https://github.com/neovim/neovim/releases/tag/v0.9.5)
- [Neovim AppImage Link](https://github.com/neovim/neovim/releases/download/v0.9.5/nvim.appimage)
- [Neovim with AppImage](https://practical.li/neovim/install/neovim/#install-neovim_1)
- [install nerd font](https://github.com/ryanoasis/nerd-fonts?tab=readme-ov-file#option-3-install-script)
- [Download Nerd-Font](https://github.com/ryanoasis/nerd-fonts/raw/HEAD/patched-fonts/DroidSansMono/DroidSansMNerdFont-Regular.otf)
- [install RUST](https://www.rust-lang.org/tools/install)
- 참고 블로그 [LunarVim 설치](https://velog.io/@mythos/Linux-Lunar-Vim-%EC%84%A4%EC%B9%98), [neovim 설정](https://velog.io/@mythos/Linux-neovim-%EC%84%A4%EC%A0%95-CoC-Vim-Plug-treesitter-NERDTree)
- [LazyVim](https://www.lazyvim.org/)
- [kickstart.nvim](https://github.com/nvim-lua/kickstart.nvim)

```bash
# 폴더 만들기
mkdir -p ~/.local/bin
# 다운로드 Neovim AppImage
wget https://github.com/neovim/neovim/releases/download/v0.9.5/nvim.appimage
# 권한 변경
chmod u+x nvim.appimage
# 복사 neovim.AppImage
cp nvim.appimage ~/.local/bin/
# 심볼릭링크 만들기
ln -s ~/.local/bin/nvim.appimage ~/.local/bin/nvim
# If your system does not have FUSE you can extract the appimage
./nvim.appimage --appimage-extract
./squashfs-root/usr/bin/nvim
ln -s /root/.local/bin/squashfs-root/usr/bin/nvim ~/.local/bin/nvim
# PATH 설정
vim ~/.bashrc
export PATH="$HOME/.local/bin:$PATH"
alias nv='nvim'
# RUST 설치 onWSL
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
# Make sure you have installed the latest version of Neovim v0.9.0+.
# Have git, make, pip, python, npm, node and cargo installed on your system.
sudo apt install cargo -y
# LunarVim 설치
LV_BRANCH='release-1.3/neovim-0.9' bash <(curl -s https://raw.githubusercontent.com/LunarVim/LunarVim/release-1.3/neovim-0.9/utils/installer/install.sh)
# nerd-font 설치 Option 6
mkdir -p ~/.local/share/fonts
cd ~/.local/share/fonts && curl -fLO https://github.com/ryanoasis/nerd-fonts/raw/HEAD/patched-fonts/DroidSansMono/DroidSansMNerdFont-Regular.otf
# nerd-font 설치하는 방법
# git clone https://github.com/ronniedroid/getnf.git
# ./getnf/install.sh
# rm -rf ./getnf
# fc-cache -f -v

# CoC 플러그인을 위해 Node.js 설치
curl -sL install-node.now.sh/lts | sudo $SHELL
```

### 환경설정 파일
{: #upj_1705714728907}

~/.config/nvim/init.vim

alias vi='nvim'
alias vim='vim'

**해결해야할 과제**

- 터미널 clipboard 연동

```shell
" =========================================================================
" =  플러그인 설정                                                        =
" =========================================================================
call plug#begin('~/.vim/plugged') " 플러그인 시작

" Conquer Of Completion 자동완성 플러그인
"Plug 'neoclide/coc.nvim', {'branch': 'release'}

" nvim-treesitter 구문 파싱 하이라이팅
Plug 'nvim-treesitter/nvim-treesitter', {'do': ':TSUpdate'}

" Tagbar 코드 뷰어 창
" Plug 'majutsushi/tagbar'
" Plug 'preservim/tagbar'

" NERDTree 코드 뷰어 창
Plug 'preservim/nerdtree'

" 컬러스킴(색상표) jellybeans, gruvbox
Plug 'nanotech/jellybeans.vim'
" Plug 'morhetz/gruvbox'

" 하단에 다양한 상태(몇 번째 줄, 인코딩, etc.)를 
" 표시하는 상태바 추가
Plug 'vim-airline/vim-airline'
Plug 'vim-airline/vim-airline-themes'

" CScope 플러그인
Plug 'ronakg/quickr-cscope.vim'

" CtrlP 파일 탐색 플러그인
Plug 'ctrlpvim/ctrlp.vim'

" 비활성 윈도우 강조
" Plug 'blueyed/vim-diminactive'

" vim cutlass 잘라내기 명령어가 yank 에 영향을 주지 않음
" Plug 'svermeulen/vim-cutlass'

" VIM GAS(GNU ASsembler) Highlighting
" Plug 'Shirk/vim-gas'

call plug#end()

" =========================================================================
" =  단축키 지정                                                          =
" =  n(normal mode) 명령 모드                                             =
" =  v(visual, select mode) 비주얼 모드                                   =
" =  x(visual mode only) 비주얼 모드                                      =
" =  s(select mode only) 선택 모드                                        =
" =  i(insert mode) 편집 모드                                             =
" =  t(terminal mode) 편집 모드                                           =
" =  c(commnad-line) 모드                                                 =
" =  re(recursive) 맵핑                                                   =
" =  nore(no recursive) 맵핑                                              =
" =========================================================================
" ------------------------------------
" 편집 모드
" ------------------------------------
" jk 와 kj 를 <ESC> 키로 맵핑
inoremap jk <ESC>
inoremap kj <ESC>
" ------------------------------------
" 명령 모드
" ------------------------------------
" <F1> 을 통해 NERDTree 와 Tagbar 열기
" nnoremap <silent><C-o> :NERDTreeToggle<CR><bar>:TagbarToggle <CR>
nnoremap <silent><C-o> :NERDTreeToggle<CR>

" <Ctrl + j, k> 를 눌러서 이전, 다음 탭으로 이동
nnoremap <silent><C-j> :tabprevious<CR>
nnoremap <silent><C-k> :tabnext<CR>

" <Ctrl + h, l> 를 눌러서 이전, 다음 버퍼로 전환
nnoremap <silent><C-h> :bp<CR>
nnoremap <silent><C-l> :bn<CR>

" <Shift + h, l> 를 눌러서 현재 버퍼 삭제
nnoremap <silent><S-h> :bp<bar>sp<bar>bn<bar>bd<CR>
nnoremap <silent><S-l> :bp<bar>sp<bar>bn<bar>bd<CR>

" <Ctrl + w> t 를 눌러서 커서를 NERDTree 로 옮기기
nnoremap <silent><C-w>t :NERDTreeFocus<CR>

" 우측 하단(botright)에 창 생성(new), 해당 창을 terminal 로 변경
" 크기를 10 으로 재설정(resize) 후 창 높이를 고정(winfixheight)시킴
" 줄번호는 삭제하고, 터미널 디렉터리 글자색을 변경
nnoremap <silent><F2>
	\:botright new<CR><bar>
	\:terminal<CR><bar><ESC>
	\:resize 10<CR><bar>
	\:set winfixheight<CR><bar>
	\:set nonu<CR><bar>
	\iLS_COLORS=$LS_COLORS:'di=1;33:ln=36'<CR>
" ------------------------------------
" 터미널 모드
" ------------------------------------
" 터미널 모드에서 <Ctrl + w> 누르면 명령 모드로 전환하고 <Ctrl + w> 입력
tmap <silent><C-w> <ESC><C-w>

" jk 혹은 kj 를 누르면 <ESC> 를 실행
tmap <silent>jk <ESC>
tmap <silent>kj <ESC>

" <ESC> 입력 시 <C-\><C-n> 실행 => 터미널 모드에서 기본 모드로 전환
tnoremap <silent><ESC> <C-\><C-n>

" ------------------------------------
" 명령, 비주얼 모드
" ------------------------------------
" iamroot 자동 주석
map <F9> <ESC>o/*<CR> * IAMROOT, <C-R>=strftime("%Y.%m.%d")<CR>
	\: <CR>*/<CR><ESC><UP><UP><END>
" =========================================================================
" =  vim 설정                                                             =
" =========================================================================
" 탭을 스페이스로 변경
set softtabstop=2
" 탭 정지 = 2 칸마다
set tabstop=2
" 쉬프트 (<< 혹은 >>) 이동거리 2 칸
set shiftwidth=2

" 줄 번호를 표시한다.
set number

" 괄호 짝을 강조한다.
set showmatch

" 하위 디렉터리를 모두 path 에 추가한다.
" gf 명령어 사용 시 파일을 인식 가능
set path+=**

" 탐색 문자열 강조
set hlsearch

" 항상 상단에 탭 라인을 출력한다.
set showtabline=2

" 행 표시선 출력
set colorcolumn=200

if has('nvim')			" nvim 을 사용 중이라면
	set inccommand=nosplit	" nvim live %s substitute (실시간 강조)
endif

" vim 과 OS 의 클립보드 동기화
" set clipboard=unnamedplus
set clipboard+=unnamedplus

" GUI-Color 를 사용 가능하도록 설정 (TrueColor)
" cterm 혹은 term 대신 gui 를 통해 색상을 설정할 수 있고
" 16,777,216 종류의 색상 표현 가능(기존 256)
set termguicolors

" 모든 마우스 기능을 사용
set mouse=a

" mkview 명령어가 저장하는 요소 중
" 하나인 `options` 를 제거
set viewoptions-=options

" 문법이 존재하면
if has("syntax")
	" 문법 강조를 수행
	syntax on
endif

" 컬러스킴(문법 강조 색상) - 현재 jellybeans
colorschem jellybeans
" colorschem gruvbox

" =========================================================================
" =  하이라이트 정의                                                      =
" =========================================================================
" 버퍼(창)과 버퍼의 끝(창의 끝)을 투명하게
highlight Normal guibg=NONE
highlight EndOfBuffer guibg=NONE

" 줄번호 배경색은 투명(NULL)하게,
" 글자는 굵게(bold), 글자색은 하얗게(White)
highlight LineNr guibg=NONE gui=bold guifg=white

" 행 표시선 색상
highlight ColorColumn guibg=White
" =========================================================================
" =  함수 정의                                                            =
" =========================================================================
" tabsize 를 size 로 변경
function SetTab(size)
	execute "set shiftwidth=".a:size
	execute "set tabstop=".a:size
	execute "set softtabstop=".a:size
endfunction
" =========================================================================
" =  자동 실행 (autocmd)                                                  =
" =========================================================================
" terminal buffer 에 진입했을 때 mode 를 normal 에서 terminal 모드로 변경
" 또한 줄번호를 없앤다.
autocmd BufEnter term://* start " do nothing
autocmd TermOpen term://* execute ":set nonu"
" =========================================================================
" =  플러그인 설정                                                        =
" =========================================================================
" ------------------------------------
" coc 설정
" ------------------------------------
"  nvim 버전이 0.5.0 이상이며, 패치가 8.1.1564 이상이라면
if has("nvim-0.5.0") || has("patch-8.1.1564")
  " 사인(sign column) 열을 숫자 열과 합침
  set signcolumn=number
endif

" <Backspace> 키가 지시자 제거, 기존 자동완성 양식 폐기
function! s:check_back_space() abort
  let col = col('.') - 1
  return !col || getline('.')[col - 1]  =~# '\s'
endfunction

" <Ctrl + Space> 를 눌러서 자동완성 적용
"if has('nvim')
"  inoremap <silent><expr> <c-space> coc#refresh()
"else
"  inoremap <silent><expr> <c-@> coc#refresh()
"endif

" 커서 아래의 토큰을 강조
"autocmd CursorHold * silent call CocActionAsync('highlight')
" ------------------------------------
" tagbar 설정
" ------------------------------------
" tagbar 생성 시 우측 하단에 위치하게끔 생성
" let g:tagbar_position = 'rightbelow'
" ------------------------------------
" vim-airline 설정
" ------------------------------------
" powerline-font 활성화
let g:airline_powerline_fonts = 1
" luna 테마 사용
let g:airline_theme = 'luna'
" tabline 에 파일명만 출력 되도록 설정
let g:airline#extensions#tabline#formatter = 'unique_tail'
" 창의 상단에 표시되도록 설정
" let g:airline_statusline_ontop = 1
" 탭라인 허용
let g:airline#extensions#tabline#enabled = 1
" 항상 tabline 을 표시
let g:airline#extensions#tabline#show_tabs = 1
" ------------------------------------
" NERDTree 설정
" ------------------------------------
" 창 크기(가로)를 20 으로 설정
let g:NERDTreeWinSize=30
" ------------------------------------
" vim-cutlass 설정
" ------------------------------------
" c, C 명령어는 yank 에 영향을 주도록 변경
" nnoremap c d
" xnoremap c d

" nnoremap cc dd
" nnoremap C Dv

" 옛날 설정파일
set noundofile
set nobackup
set nowritebackup
set noswapfile
set fileencodings=utf8,euc-kr
set autowrite
set autowriteall

augroup markdownindent
  autocmd FileType markdown setlocal expandtab
  autocmd FileType markdown setlocal tabstop=2
  autocmd FileType markdown setlocal shiftwidth=2
augroup END
```

## 패키지 설치 업데이트 업그레이드
{: #upj_1676507824297}

```shell
     패키지 관리자
apt update -y
apt upgrade -y
apt list –installed
apt install 패키지명
apt remove 설정 유지하고 삭제
apt purge  설정까지 삭제

     저장소(repository) 살펴보기
/etc/apt/* 각종 설정들 확인

     저장소 추가/삭제
sudo add-apt-repository ppa:주소
sudo add-apt-repository --remove ppa:주소

     dpkg 설치 (데비안 패키지 관리자)
dpkg -i 패키지명	설치
dpkg -r 패키지명	설정 유지하고 삭제
dpkg -P 패키지명	설정까지 삭제
dpkg -l 		설치된 패키지 목록 보기
sudo dpkg -i  google-chrome-stable_current_amd64.deb

     운영체제 업그레이드
sudo apt update
sudo apt upgrade
sudo do-release-upgrade
```

## 데몬 서비스 관리하기
{: #upj_1676507830185}

데몬
: 사용자가 직접적으로 제어하지 않고, 백그라운드에서 돌면서 여러 작업을 하는 프로그램

서비스
: 서버/클라이언트 모델에서 출발하여, 사용자의 요청에 응답하는 프로그램
: 주로 데몬 형태로 구동됨
: (사용예) httpd, ftpd, sshd..

```shell
     서비스 관리하기
systemctl status
systemctl status 데몬명.service
systemctl start 데몬명	(생략가능)
systemctl stop 데몬명
systemctl restart 데몬명
systemctl enable 데몬명 (부팅시 자동시작)
systemctl disable 데몬명 (부팅시 자동시작 삭제)
systemctl deamon-reload 데몬 라이브러리 갱신
systemctl cat 데몬명	(설정 살펴보기)
systemctl edit --full 데몬명 (서비스 명령 수정하기)

     서비스 로그 살펴보기
journalctl		전체로그
journalctl -b		부팅후 로그
journalctl -f 최근 로그 및 이후 로그 트래킹 대기
```
