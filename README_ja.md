# 設定

私のツールの設定/構成ファイル。

---

# 開発環境(Windows向け)

自分の使っている開発ツールや設定を晒しておく。

## 開発ツール

### エディタ

* [サクラエディタ](https://github.com/sakura-editor/sakura/releases)
* [Visual Studio Code](https://code.visualstudio.com/)

### Terminal

* [PuTTY](https://www.putty.org/)
* [Windows Terminal](https://www.microsoft.com/ja-jp/p/windows-terminal/9n0dx20hk701?activetab=pivot:overviewtab)
* [Tera Term](https://forest.watch.impress.co.jp/library/software/utf8teraterm/)

### DBアクセス

* [A5SQL Mk2](https://a5m2.mmatsubara.com/)
* [MySQL Workbench](https://www.mysql.com/jp/products/workbench/)

### 統合開発環境

* [PHP Storm](https://www.jetbrains.com/ja-jp/phpstorm/)
* [Eclipse PHP Development Tools](https://www.eclipse.org/pdt/)

### Git

* [Git for Windows](https://gitforwindows.org/)
* [Source Tree](https://www.sourcetreeapp.com/)

### 差分比較/マージ

* [WinMerge](https://winmergejp.bitbucket.io/)

### 仮想マシン

* [Docker for Windows](https://docs.docker.com/docker-for-windows/install/)

### ドキュメント生成

* [Doxygen](http://www.doxygen.jp/)
* [Graphviz](https://www.graphviz.org/)

### 圧縮/解凍

* [Lhaplus](https://forest.watch.impress.co.jp/library/software/lhaplus/)

### 画像編集

* [JTrim](https://forest.watch.impress.co.jp/library/software/jtrim/)
* [GIMP](https://forest.watch.impress.co.jp/library/software/gimp/)

### WSL(Windows Subsystem for Linux)追加パッケージ

Ubuntu 18.04

パッケージ最新化

```sh
sudo apt -y update
sudo apt -y upgrade
sudo apt -y autoremove
```

追加パッケージインストール

```sh
sudo apt -y install \
build-essential \
python3 \
python3-pip \
python3-dev \
vim \
vim-scripts \
screen \
language-pack-ja \
mysql-client \
nkf \
jq
```

追加設定

```sh
sudo update-locale LANG=ja_JP.UTF8
sudo dpkg-reconfigure tzdata
echo "set bell-style none" >> ~/.inputrc
echo "set visualbell t_vb=" >> ~/.vimrc
echo "export SCREENDIR=$HOME/.screen" >> ~/.bashrc
echo "umask 022" >> ~/.bashrc
echo "alias python=python3" >> ~/.bashrc
echo "alias docker='/mnt/c/Program\ Files/Docker/Docker/resources/bin/docker.exe'" >> ~/.bashrc
```

Windowsのディレクトリへの移動を簡単にするため、シンボリックリンクを作成しておく

```sh
ln -s /mnt/c/Users/[Windowsのログインユーザー名]/Documents Documents
ln -s /mnt/c/Users/[Windowsのログインユーザー名]/Downloads Downloads
```

WSL Ubuntuのデフォルトのディレクトリ表示色は見辛いので変更する。

```
dircolors -p > ~/.dircolors
```

出力された `~/.dircolors` を編集して、以下の値を書き換える

* OTHER_WRITABLE<br>
01;42 を 01;32 に変更。
* STICKY_OTHER_WRITABLE<br>
30;42 を 30;32 に変更。

### VSCodeで文字コードの自動判定

Settings.json で以下の項目を探して trueにする。<br>
(最新の「設定」画面ではチェックボックスになっているので ON にするだけでOK)

```json
"files.autoGuessEncoding": true
```

但し、時々判定に失敗するので、そのときは手動で文字コードを指定して開き直す必要がある。

## 拡張機能

### Google Chrome

* [AutoPagerize](https://chrome.google.com/webstore/detail/chrome-remote-desktop/inomeogfingihgjfjlpeplalcfajhgai)
* [AMP Validator](https://chrome.google.com/webstore/detail/amp-validator/nmoffdblmcmgeicmolmhobpoocbbmknc)
* [Chrome Remote Desktop](https://chrome.google.com/webstore/detail/chrome-remote-desktop/inomeogfingihgjfjlpeplalcfajhgai)
* [cocopy](https://chrome.google.com/webstore/detail/cocopy/ihnfodlbkhgjnbheemjhkjfkfglgbdgc)
* [EditThisCookie](https://chrome.google.com/webstore/detail/editthiscookie/fngmhnnpilhplaeedifhccceomclgfbg)
* [Google translate](https://chrome.google.com/webstore/detail/google-translate/aapbdbdomjkkjkaonfhkkikfgjllcleb)
* [Improve YouTube! (Video & YouTube Tools)🎧](https://chrome.google.com/webstore/detail/improve-youtube-video-you/bnomihfieiccainjcjblhegjgglakjdd)
* [GoFullPage - Full Page Screen Capture](https://chrome.google.com/webstore/detail/gofullpage-full-page-scre/fdpohaocaechififmbbbbbknoalclacl)
* [Google Mail Checker](https://chrome.google.com/webstore/detail/google-mail-checker/mihcahmgecmbnbcchbopgniflfhgnkff)
* [Google Offline Document](https://chrome.google.com/webstore/detail/google-docs-offline/ghbmnnjooekpmoecnnnilnnbdlolhkhi)
* [LTTM](https://chrome.google.com/webstore/detail/lttm/jdidcgkdggndpodjbipodfefnpgjooeh)
* [Pegmatite](https://chrome.google.com/webstore/detail/pegmatite/jegkfbnfbfnohncpcfcimepibmhlkldo)
* [Picture-in-Picture Extension (by Google)](https://chrome.google.com/webstore/detail/picture-in-picture-extens/hkgfoiooedgoejojocmhlaklaeopbecg)
* [RSS Subscription Extension（by Google）](https://chrome.google.com/webstore/detail/rss-subscription-extensio/nlbjncdgjeocebhnmkbbbdekmmmcbfjd)
* [Screenshot YouTube](https://chrome.google.com/webstore/detail/screenshot-youtube/gjoijpfmdhbjkkgnmahganhoinjjpohk)
* [twitter Image full size button](https://chrome.google.com/webstore/detail/twitter%E7%94%BB%E5%83%8F%E5%8E%9F%E5%AF%B8%E3%83%9C%E3%82%BF%E3%83%B3/kmcomcgcopagkhcbmcmcfhpcmdolfijg)
* [Vein: a New Social Reading Service.](https://chrome.google.com/webstore/detail/vein-a-new-social-reading/enbmoagmhglhpniadofemlmhpjhncpna)
* [Hatena Bookmark](https://chrome.google.com/webstore/detail/%E3%81%AF%E3%81%A6%E3%81%AA%E3%83%96%E3%83%83%E3%82%AF%E3%83%9E%E3%83%BC%E3%82%AF/dnlfpnhinnjdgmjfpccajboogcjocdla)
* [Application Launcher for Drive (Google)](https://chrome.google.com/webstore/detail/application-launcher-for/lmjegmlicamnimmfhcmpkclmigmmcbeh)

### Google Chrome Apps

* [Caret](https://chrome.google.com/webstore/detail/caret/fljalecfjciodhpcledpamjachpmelml)
* [Text](https://chrome.google.com/webstore/detail/text/mmfbcljfglbokpmkimbfghdkjmjhdgbg)
* [Web Server for Chrome](https://chrome.google.com/webstore/detail/web-server-for-chrome/ofhbbkphhbklhfoeikjpcbhemlocgigb)
* [Chrome MySQL Admin](https://chrome.google.com/webstore/detail/chrome-mysql-admin/ndgnpnpakfcdjmpgmcaknimfgcldechn)
* [Zoom](https://chrome.google.com/webstore/detail/zoom/hmbjbjdpkobdjplfobhljndfdfdipjhg)
* [Spreadsheet](https://chrome.google.com/webstore/detail/sheets/felcaaldnbdncclmgdcncolpebgiejap)
* [Slide](https://chrome.google.com/webstore/detail/slides/aapocclcgogkmnckokdopfmhonfmgoek)
* [Document](https://chrome.google.com/webstore/detail/docs/aohghmighlieiainnegkcijnfilokake)

### Visualstudio Code

* [.NET Install Tool for Extension Authors](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.vscode-dotnet-runtime)
* [Auto Rename Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-rename-tag)
* [AWS Toolkit](https://marketplace.visualstudio.com/items?itemName=AmazonWebServices.aws-toolkit-vscode)
* [Azure Tools](https://marketplace.visualstudio.com/items?itemName=ms-vscode.vscode-node-azure-pack)
    * [Azure App Service](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-azureappservice)
    * [Azure CLI Tools](https://marketplace.visualstudio.com/items?itemName=ms-vscode.azurecli)
    * [Azure Databases](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-cosmosdb)
    * [Azure Functions](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-azurefunctions)
    * [Azure Pipelines](https://marketplace.visualstudio.com/items?itemName=ms-azure-devops.azure-pipelines)
    * [Azure Resources](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-azureresourcegroups)
    * [Azure Resource Manager (ARM) Tools](https://marketplace.visualstudio.com/items?itemName=msazurermtools.azurerm-vscode-tools)
    * [Azure Storage](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-azurestorage)
    * [Azure Virtual Machines](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-azurevirtualmachines)
    * [Bicep](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-bicep)
    * [Docker](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-docker)
    * [ARM Template Viewer](https://marketplace.visualstudio.com/items?itemName=bencoleman.armview)
* [Azure Account](https://marketplace.visualstudio.com/items?itemName=ms-vscode.azure-account)
* [Azure Kubernetes Service](https://marketplace.visualstudio.com/items?itemName=ms-kubernetes-tools.vscode-aks-tools)
* [Azure Machine Learning](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.vscode-ai)
* [Azure Machine Learning - Remote](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.vscode-ai-remote)
* [C/C++](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools)
* [Debugger for Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge)
* [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker)
* [Draw.io Integration](https://marketplace.visualstudio.com/items?itemName=hediet.vscode-drawio)
* [Encode Decode](https://marketplace.visualstudio.com/items?itemName=mitchdenny.ecdc)
* [Excel to Markdown table](https://marketplace.visualstudio.com/items?itemName=csholmq.excel-to-markdown-table)
* [Excel Viewer](https://marketplace.visualstudio.com/items?itemName=GrapeCity.gc-excelviewer)
* [File Utils](https://marketplace.visualstudio.com/items?itemName=sleistner.vscode-fileutils)
* [Git Graph](https://marketplace.visualstudio.com/items?itemName=mhutchie.git-graph)
* [GitHub](https://marketplace.visualstudio.com/items?itemName=KnisterPeter.vscode-github)
* [GitHub Copilot](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot)
* [GitHub Pull Requests and Issues](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github)
* [GitHub Repositories](https://marketplace.visualstudio.com/items?itemName=GitHub.remotehub)
* [GitLens — Git supercharged](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)
* [Google Translate](https://marketplace.visualstudio.com/items?itemName=hancel.google-translate)
* [Hasher](https://marketplace.visualstudio.com/items?itemName=deerawan.vscode-hasher)
* [Hex Editor](https://marketplace.visualstudio.com/items?itemName=ms-vscode.hexeditor)
* [Image preview](https://marketplace.visualstudio.com/items?itemName=kisstkondoros.vscode-gutter-preview)
* [Japanese Language Pack for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=MS-CEINTL.vscode-language-pack-ja)
* [Jupyter](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter)
* [Jupyter Keymap](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter-keymap)
* [Jupyter Notebook Renderers](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter-renderers)
* [Kubernetes](https://marketplace.visualstudio.com/items?itemName=ms-kubernetes-tools.vscode-kubernetes-tools)
* [Live Sass Compiler](https://marketplace.visualstudio.com/items?itemName=ritwickdey.live-sass)
* [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)
* [Markdown Preview Enhanced](https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced)
* [Material Icon Theme](https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme)
* [Open to Other Editor Group](https://marketplace.visualstudio.com/items?itemName=shibayu36.open-to-other-editor-group)
* [PlantUML](https://marketplace.visualstudio.com/items?itemName=jebbs.plantuml)
* [Pylance](https://marketplace.visualstudio.com/items?itemName=ms-python.vscode-pylance)
* [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python)
* [Remote Development](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack)
    * [Remote - WSL](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl)
    * [Remote - Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)
    * [Remote - SSH](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-ssh)
    * [Remote - SSH: Editing Configuration Files](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-ssh-edit)
* [REST Client](https://marketplace.visualstudio.com/items?itemName=humao.rest-client)
* [SCSS IntelliSense](https://marketplace.visualstudio.com/items?itemName=mrmlnc.vscode-scss)
* [SQLite](https://marketplace.visualstudio.com/items?itemName=alexcvzz.vscode-sqlite)
* [TSLint](https://marketplace.visualstudio.com/items?itemName=ms-vscode.vscode-typescript-tslint-plugin)
* [Vscode Google Translate](https://marketplace.visualstudio.com/items?itemName=funkyremi.vscode-google-translate)
* [VSCode Ruby](https://marketplace.visualstudio.com/items?itemName=wingrunr21.vscode-ruby)
* [vscode-icons](https://marketplace.visualstudio.com/items?itemName=vscode-icons-team.vscode-icons)
* [vscode-reveal](https://marketplace.visualstudio.com/items?itemName=evilz.vscode-reveal)
* [YAML](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml)

### 追加設定

Ctrl + ,のショートカット、もしくは File > Preferences > Settings で移動。

* VS Codeの統合ターミナルをGitBashにする
検索欄に terminal.integrated.shell.windows を打ち込み、settings.jsonで編集 で編集画面表示。以下の内容を記述する。

```json
"terminal.integrated.shell.windows": "C:\\Program Files\\Git\\bin\\bash.exe",
```

* 改行コード
検索欄に files.eol を打ち込み、ドロップダウンリストで "\n" を選択してデフォルトの改行コードをLFに変更する。
もしくはsettings.jsonで以下の項目を記述する。

```json
"files.eol": "\n",
```

* 文字コード自動判定
検索欄に files.autoGuessEncoding  を打ち込み、チェックボックスを ON にする。
もしくはsettings.jsonで以下の項目を記述する。

```json
"files.autoGuessEncoding": true,
```

* REST Client
デフォルトのままだと戻ってくるJSONに日本語が含まれてると文字化けするので、検索欄に rest-client.decodeEscapedUnicodeCharacter を打ち込み、チェックボックスを ON にする。
もしくはsettings.jsonで以下の項目を記述する。

```json
"rest-client.decodeEscapedUnicodeCharacters": true,
```

* 単語区切り
句読点を単語と見做してくれるので、Ctrl+Alt(Opt)+F/B やAlt(Opt)←→で句読点までジャンプできる。検索欄に editor.wordSeparators を打ち込み、"`~!@#$%^&*()-=+[{]}\\|;:'\",.<>/?、。　" を上書きする。
もしくはsettings.jsonで以下の項目を記述する。

```json
"editor.wordSeparators": "`~!@#$%^&*()-=+[{]}\\|;:'\",.<>/?、。　",
```

* アクティブな編集タブの背景色
デフォルトだと見づらいので、変更する。検索欄に workbench.colorCustomizations を打ち込み、settings.jsonで以下の項目を記述する。

```json
    "workbench.colorCustomizations": {
        "tab.activeBackground": "#0184bc"
    },
```

---

## テーマ

### Visual Studio Code

* [Atom One Dark Theme](https://marketplace.visualstudio.com/items?itemName=akamud.vscode-theme-onedark)
* [Atom One Light Theme](https://marketplace.visualstudio.com/items?itemName=akamud.vscode-theme-onelight)
* [Helium Icon Theme](https://marketplace.visualstudio.com/items?itemName=jumpinjackie.vscode-map-preview)

### vim

* [shirotelin](https://github.com/yasukotelin/shirotelin)
* [One Half](https://github.com/sonph/onehalf)

---

# 手順

## 鍵ファイルの変換

PuTTY形式 から sshコマンドなどで使うための Openssh形式に変換した鍵を作成する。

### 変換方法

1. スタートメニューから [PuTTY Gen(PuTTY Key Generator)] を起動する。
2. [File]-[Load private key] で PuTTY形式の鍵ファイルを読み込む。
3. [Conversions]-[Export OpenSSH key]を選択する。
4. パスフレーズで保護しなくて良いか？確認するダイアログボックスが表示されるので [はい] を選択する。
5. ファイル名を入力して保存する。便宜上、元ファイル名(*.ppk)の拡張子を .pem にしたものを推奨。
6. 生成された鍵ファイルを `~/.ssh/` の下にコピーする。
    * Windowsの場合は `~/` の配下以外に鍵ファイルを置くと接続エラーになる。
    * Linuxの場合はコピー後にパーミッションを自分のみ読み書きできるように変更しないと接続エラーになる。
    ```sh
    chmod 600 ~/.ssh/*.pem
    ```

---

# 設定ファイル

## ~/.bashrc

* Gitbash用。以下はWSLのUbuntuのもののコピー。
* Windowsの場合は `C:\Users\[ログインユーザー名]` 直下がホームディレクトリ(~/)

```sh
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
    PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\]\$ '
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

# some more ls aliases
alias ll='ls -alF'
alias la='ls -A'
alias l='ls -CF'

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
```

追加のエイリアス設定(Windows GitBash)

```sh
alias cp='cp -i'
alias rm='rm -i'
alias mv='mv -i'
alias crontab='crontab -i'
alias view='vim -R'
alias vimdiff='vim -d'
alias curl='curl -s'
alias ssh='ssh -o ServerAliveInterval=60'
export LANG=ja_JP.UTF-8
function _compreply_ssh(){
  COMPREPLY=(`cat ~/.ssh/config | grep -i -e '^host' | cut -d " " -f 2 | grep -E "$2"`)
}
complete -F _compreply_ssh ssh
alias tree='tree.com' 
```

追加のエイリアス設定(WSL Ubuntu)

```sh
export SCREENDIR=$HOME/.screen
alias crontab='crontab -i'
export SCREENDIR=/home/kabukawa/.screen
umask 022
alias python=python3
alias docker='/mnt/c/Program\ Files/Docker/Docker/resources/bin/docker.exe'
eval $(dircolors -b ~/.dircolors)
complete -C '/usr/local/bin/aws_completer' aws
```

## ~/.gitconfig(Windows)

* Windowsの場合は `C:\Users\[ログインユーザー名]` 直下がホームディレクトリ(~/)
* {ユーザー名}と{メールアドレス}は自分のものに置き換えること。

```ini
[user]
	name = {ユーザー名}
	email = {メールアドレス}
[credential "helperselector"]
    selected = <no helper>
[diff]
    tool = vimdiff
[difftool]
    prompt = false
[merge]
    tool = vimdiff
[mergetool]
    prompt = false
[difftool "sourcetree"]
    cmd = 'C:/Program Files/WinMerge/WinMergeU.exe' \"$LOCAL\" \"$REMOTE\"
[mergetool "sourcetree"]
    cmd = 'C:/Program Files/WinMerge/WinMergeU.exe' -e -ub -fr -ar -wl -wm -dl base -dm remote -dr local $BASE $REMOTE $LOCAL -o $MERGED
    trustExitCode = true
[core]
    quotepath = false
```

## ~/.gitconfig(Linux)

* {ユーザー名}と{メールアドレス}は自分のものに置き換えること。

```ini
[user]
    name = {ユーザー名}
    email = {メールアドレス}
[diff]
    tool = vimdiff
[difftool]
    prompt = false
[merge]
    tool = vimdiff
[mergetool]
    prompt = false
```

## ~/.vimrc

* Windowsの場合は `C:\Users\[ログインユーザー名]` 直下がホームディレクトリ(~/)

```vim
colorscheme onehalfdark
syntax on
set hlsearch
set ts=4
set nowrap
set belloff=all
set laststatus=2
set showmatch
set cursorline
set fileformats=unix,dos,mac
set encoding=utf-8
set fileencodings=iso-2022-jp,cp932,sjis,euc-jp,utf-8
highlight CursorLine cterm=underline ctermfg=NONE ctermbg=NONE
highlight CursorLine gui=underline guifg=NONE guibg=NONE
highlight StatusLine term=none cterm=none ctermfg=black ctermbg=darkblue
```

## ~/.screenrc

```sh
defutf8 on
defencoding utf8
encoding utf8 utf8

startup_message off
vbell off

# 色
# オレンジが赤になるとかならscreenが256色対応じゃないかも
# FYI: https://qiita.com/trapple/items/8ad1b0a7c4fa5b8341b0
# $ brew tap homebrew/dupes
# $ brew install screen
defbce on
term xterm-256color


# ステータスライン
hardstatus alwayslastline "%{= cd} %-w%{= wk} %n %t* %{-}%+w %= LoadAVG [%l] "

# エスケープキー
#escape ^Tt

# マウススクロール
termcapinfo xterm* ti@:te@

# スクロール行数
defscrollback 10000

# vimとかlessとかtigとかのバッファを終了時に消す
altscreen on

# デフォルトシェル
shell $SHELL
```

## ~/.ssh/config

* Windowsの場合は `C:\Users\[ログインユーザー名]` 直下がホームディレクトリ(~/)
* Linuxの場合は `~/.ssh/` の下は自分のみ読み書き可能なるようにパーミッションを変更する。
* {ユーザー名}と{鍵ファイル名}は自分のものに置き換えること。

```sh
## develop
Host {ホスト名}
  HostName {IPアドレス}
  User {ユーザー名}
  IdentityFile ~/.ssh/{鍵ファイル名}
```

* 環境名をログイン後のプロンプトに出したい場合

```sh
## develop
Host {ホスト名}
  HostName {IPアドレス}
  User {ユーザー名}
  IdentityFile ~/.ssh/{鍵ファイル名}
  RequestTTY yes
  RemoteCommand PS1="\[\e[1;32m\][\u@\h \w] [環境名] $ \[\e[m\]" bash --login
```

## ~/.my.cnf 

```ini
[client]
host={ホスト名}
user={ユーザー名}
password={パスワード}
port=3306
database={スキーマ名}
```