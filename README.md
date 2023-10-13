# settings

My tools setting/configurarion files.

---

# Development environment (for Windows)

Expose the development tools and settings you are using.

## Development tools

### Editor

* [Sakura Editor](https://github.com/sakura-editor/sakura/releases)
* [Visual Studio Code](https://code.visualstudio.com/)

### Terminal

* [PuTTY](https://www.putty.org/)
* [Windows Terminal](https://www.microsoft.com/ja-jp/p/windows-terminal/9n0dx20hk701?activetab=pivot:overviewtab)
* [Tera Term](https://forest.watch.impress.co.jp/library/software/utf8teraterm/)

### DB access

* [A5SQL Mk2](https://a5m2.mmatsubara.com/)
* [MySQL Workbench](https://www.mysql.com/jp/products/workbench/)
* [Data Grip](https://www.jetbrains.com/ja-jp/datagrip/)
* [MongoDB Compass](https://www.mongodb.com/try/download/shell)

### Integrated development environment

* [PHP Storm](https://www.jetbrains.com/ja-jp/phpstorm/)
* [Eclipse PHP Development Tools](https://www.eclipse.org/pdt/)
* [RubyMine](https://www.jetbrains.com/ja-jp/ruby/)

### Git

* [Git for Windows](https://gitforwindows.org/)
* [Source Tree](https://www.sourcetreeapp.com/)

### Difference comparison / merge

* [WinMerge](https://winmergejp.bitbucket.io/)

### Virtual machine

* [Docker for Windows](https://docs.docker.com/docker-for-windows/install/)

### Document generation

* [Doxygen](http://www.doxygen.jp/)
* [Graphviz](https://www.graphviz.org/)

### Compress / decompress

* [Lhaplus](https://forest.watch.impress.co.jp/library/software/lhaplus/)

### image editing

* [JTrim](https://forest.watch.impress.co.jp/library/software/jtrim/)
* [GIMP](https://forest.watch.impress.co.jp/library/software/gimp/)

### Cloud CLI

* [Azure CLI](https://aka.ms/installazurecliwindows)
* [AWS CLI](https://awscli.amazonaws.com/AWSCLIV2.msi)
* [AWS Session Manager Plugin](https://s3.amazonaws.com/session-manager-downloads/plugin/latest/windows/SessionManagerPluginSetup.exe)
* [Heroku CLI](https://devcenter.heroku.com/ja/articles/heroku-cli#install-the-heroku-cli)

### Utility

* [DevToys](https://apps.microsoft.com/store/detail/devtoys/9PGCV4V3BK4W?hl=ja-jp&gl=jp)

### WSL (Windows Subsystem for Linux) additional package

Ubuntu 18.04/20.04

Package update

```sh
sudo apt -y update
sudo apt -y upgrade
sudo apt -y autoremove
```

Install additional packages

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

Additional settings

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

Create a symbolic link to make it easier to navigate to a Windows directory

```sh
ln -s /mnt/c/Users/[Windows login username]/Documents Documents
ln -s /mnt/c/Users/[Windows login username]/Downloads Downloads
```

The default directory display color of WSL Ubuntu is hard to see, so change it.

```
dircolors -p > ~/.dircolors
```

Edit the output `~/.dircolors` and rewrite the following values

* OTHER_WRITABLE<br>
Changed 01;42 to 01;32.
* STICKY_OTHER_WRITABLE<br>
Changed 30;42 to 30;32.

### VS Code automatically determines character code

Find the following item in Settings.json and set it to true.<br>
(Since it is a check box on the latest "Settings" screen, you can just turn it on.)

```json
"files.autoGuessEncoding": true
```

However, sometimes the judgment fails, so in that case it is necessary to manually specify the character code and reopen.

## Extensions

### Google Chrome

* [AutoPagerize](https://chrome.google.com/webstore/detail/chrome-remote-desktop/inomeogfingihgjfjlpeplalcfajhgai)
* [AMP Validator](https://chrome.google.com/webstore/detail/amp-validator/nmoffdblmcmgeicmolmhobpoocbbmknc)
* [Chrome Remote Desktop](https://chrome.google.com/webstore/detail/chrome-remote-desktop/inomeogfingihgjfjlpeplalcfajhgai)
* [cocopy](https://chrome.google.com/webstore/detail/cocopy/ihnfodlbkhgjnbheemjhkjfkfglgbdgc)
* [EditThisCookie](https://chrome.google.com/webstore/detail/editthiscookie/fngmhnnpilhplaeedifhccceomclgfbg)
* [Google translate](https://chrome.google.com/webstore/detail/google-translate/aapbdbdomjkkjkaonfhkkikfgjllcleb)
* [e-Tax AP](https://chrome.google.com/webstore/detail/e-tax-ap/hopiajgbpnepghlkfmdonpgdnmcajpeb)
* [Improve YouTube! (Video & YouTube Tools)🎧](https://chrome.google.com/webstore/detail/improve-youtube-video-you/bnomihfieiccainjcjblhegjgglakjdd)
* [GoFullPage - Full Page Screen Capture](https://chrome.google.com/webstore/detail/gofullpage-full-page-scre/fdpohaocaechififmbbbbbknoalclacl)
* [Google Mail Checker](https://chrome.google.com/webstore/detail/google-mail-checker/mihcahmgecmbnbcchbopgniflfhgnkff)
* [Google Offline Document](https://chrome.google.com/webstore/detail/google-docs-offline/ghbmnnjooekpmoecnnnilnnbdlolhkhi)
* [Google Transrate](https://chrome.google.com/webstore/detail/google-translate/aapbdbdomjkkjkaonfhkkikfgjllcleb)
* [Lighthouse](https://chrome.google.com/webstore/detail/lighthouse/blipmdconlkpinefehnmjammfjpmpbjk)
* [LINE](https://chrome.google.com/webstore/detail/line/ophjlpahpchlmihnnnihgmmeilfjmjjc)
* [LTTM](https://chrome.google.com/webstore/detail/lttm/jdidcgkdggndpodjbipodfefnpgjooeh)
* [Pegmatite](https://chrome.google.com/webstore/detail/pegmatite/jegkfbnfbfnohncpcfcimepibmhlkldo)
* [Picture-in-Picture Extension (by Google)](https://chrome.google.com/webstore/detail/picture-in-picture-extens/hkgfoiooedgoejojocmhlaklaeopbecg)
* [RSS Subscription Extension（by Google）](https://chrome.google.com/webstore/detail/rss-subscription-extensio/nlbjncdgjeocebhnmkbbbdekmmmcbfjd)
* [Screenshot YouTube](https://chrome.google.com/webstore/detail/screenshot-youtube/gjoijpfmdhbjkkgnmahganhoinjjpohk)
* [twitter Image full size button](https://chrome.google.com/webstore/detail/twitter%E7%94%BB%E5%83%8F%E5%8E%9F%E5%AF%B8%E3%83%9C%E3%82%BF%E3%83%B3/kmcomcgcopagkhcbmcmcfhpcmdolfijg)
* [Vein: a New Social Reading Service.](https://chrome.google.com/webstore/detail/vein-a-new-social-reading/enbmoagmhglhpniadofemlmhpjhncpna)
* [ZenHub for GitHub](https://chrome.google.com/webstore/detail/zenhub-for-github/ogcgkffhplmphkaahpmffcafajaocjbd)
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
* [Better Haml](https://marketplace.visualstudio.com/items?itemName=karunamurti.haml)
* [Bicep](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-bicep)
* [Bridge to Kubernetes](https://marketplace.visualstudio.com/items?itemName=mindaro.mindaro)
* [C/C++](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools)
* [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker)
* [Debugger for Java](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-debug)
* [Debugger for Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge)
* [Dependency Analytics](https://marketplace.visualstudio.com/items?itemName=redhat.fabric8-analytics)
* [Docker](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-docker)
* [Draw.io Integration](https://marketplace.visualstudio.com/items?itemName=hediet.vscode-drawio)
* [Encode Decode](https://marketplace.visualstudio.com/items?itemName=mitchdenny.ecdc)
* [Excel to Markdown table](https://marketplace.visualstudio.com/items?itemName=csholmq.excel-to-markdown-table)
* [Excel Viewer](https://marketplace.visualstudio.com/items?itemName=GrapeCity.gc-excelviewer)
* [File Utils](https://marketplace.visualstudio.com/items?itemName=sleistner.vscode-fileutils)
* [Git Graph](https://marketplace.visualstudio.com/items?itemName=mhutchie.git-graph)
* [GitHub](https://marketplace.visualstudio.com/items?itemName=KnisterPeter.vscode-github)
* [GitHub Copilot](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot)
* [GitHub Copilot Labs](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot-labs)
* [GitHub Pull Requests and Issues](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github)
* [GitHub Repositories](https://marketplace.visualstudio.com/items?itemName=GitHub.remotehub)
* [GitLens — Git supercharged](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)
* [GlassIt-VSC](https://marketplace.visualstudio.com/items?itemName=s-nlf-fh.glassit)
* [Hasher](https://marketplace.visualstudio.com/items?itemName=deerawan.vscode-hasher)
* [Hex Editor](https://marketplace.visualstudio.com/items?itemName=ms-vscode.hexeditor)
* [Image preview](https://marketplace.visualstudio.com/items?itemName=kisstkondoros.vscode-gutter-preview)
* [IntelliCode](https://marketplace.visualstudio.com/items?itemName=VisualStudioExptTeam.vscodeintellicode)
* [Japanese Language Pack for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=MS-CEINTL.vscode-language-pack-ja)
* [Jupyter](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter)
* [Jupyter Keymap](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter-keymap)
* [Jupyter Notebook Renderers](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter-renderers)
* [Kubernetes](https://marketplace.visualstudio.com/items?itemName=ms-kubernetes-tools.vscode-kubernetes-tools)
* [Language Support for Java(TM) by Red Hat](https://marketplace.visualstudio.com/items?itemName=redhat.java)
* [Live Sass Compiler](https://marketplace.visualstudio.com/items?itemName=ritwickdey.live-sass)
* [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)
* [Live Share](https://marketplace.visualstudio.com/items?itemName=MS-vsliveshare.vsliveshare)
* [Live Share Audio](https://marketplace.visualstudio.com/items?itemName=MS-vsliveshare.vsliveshare-audio)
* [Live Share Extension Pack](https://marketplace.visualstudio.com/items?itemName=MS-vsliveshare.vsliveshare-pack)
* [Markdown Preview Enhanced](https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced)
* [Markdown Preview Github Styling](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-preview-github-styles)
* [Markdown Preview Mermaid Support](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-mermaid)
* [Material Icon Theme](https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme)
* [Marp for VS Code](https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode)
* [MongoDB for VS Code](https://marketplace.visualstudio.com/items?itemName=mongodb.mongodb-vscode)
* [Open to Other Editor Group](https://marketplace.visualstudio.com/items?itemName=shibayu36.open-to-other-editor-group)
* [PlantUML](https://marketplace.visualstudio.com/items?itemName=jebbs.plantuml)
* [Power Mode](https://marketplace.visualstudio.com/items?itemName=hoovercj.vscode-power-mode)
* [Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
* [Project Manager for Java](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-dependency)
* [Pylance](https://marketplace.visualstudio.com/items?itemName=ms-python.vscode-pylance)
* [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python)
* [Remote Development](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack)
    * [Remote - WSL](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl)
    * [Remote - Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)
    * [Remote - SSH](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-ssh)
    * [Remote - SSH: Editing Configuration Files](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-ssh-edit)
* [Remote Repositories](https://marketplace.visualstudio.com/items?itemName=ms-vscode.remote-repositories)
* [REST Book](https://marketplace.visualstudio.com/items?itemName=tanhakabir.rest-book)
* [REST Client](https://marketplace.visualstudio.com/items?itemName=humao.rest-client)
* [SCSS IntelliSense](https://marketplace.visualstudio.com/items?itemName=mrmlnc.vscode-scss)
* [SQLite](https://marketplace.visualstudio.com/items?itemName=alexcvzz.vscode-sqlite)
* [Swagger Viewer](https://marketplace.visualstudio.com/items?itemName=Arjun.swagger-viewer)
* [Test Runner for Java](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-test)
* [TSLint](https://marketplace.visualstudio.com/items?itemName=ms-vscode.vscode-typescript-tslint-plugin)
* [VSCode Ruby](https://marketplace.visualstudio.com/items?itemName=wingrunr21.vscode-ruby)
* [vscode-icons](https://marketplace.visualstudio.com/items?itemName=vscode-icons-team.vscode-icons)
* [vscode-reveal](https://marketplace.visualstudio.com/items?itemName=evilz.vscode-reveal)
* [YAML](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml)

### Additional settings

Move with Ctrl +, shortcut or File> Preferences> Settings.

* Make VS Code's integrated terminal Git Bash
Type terminal.integrated.shell.windows in the search field and edit with settings.json to display the edit screen. Describe the following contents.

```json
"terminal.integrated.shell.windows": "C:\\Program Files\\Git\\bin\\bash.exe",
```

* Line feed code
Type files.eol in the search field and select "\ n" in the drop-down list to change the default line feed code to LF.
Or describe the following items in settings.json.

```json
"files.eol": "\n",
```

* Automatic character code judgment
Type files.autoGuessEncoding in the search field and select the check box.
Or describe the following items in settings.json.

```json
"files.autoGuessEncoding": true,
```

* REST Client
If you keep the default, the returned JSON will be garbled if it contains Japanese, so type rest-client.decodeEscapedUnicodeCharacter in the search field and select the check box.
Or describe the following items in settings.json.

```json
"rest-client.decodeEscapedUnicodeCharacters": true,
```

* Word separator
Punctuation marks are considered as words, so you can use Ctrl+Alt(Opt)+F/B or Alt(Opt)←→ to jump to a punctuation mark. Type editor.wordSeparators in the search field and type "`~!@#$%^&*()-=+[{]}\\|;:'\",.<>/?、。　" to override it.
Or write the following in settings.json

```json
"editor.wordSeparators": "`~!@#$%^&*()-=+[{]}\\|;:'\",.<>/?、。　",
```

* Background color of the active editing tab
The default is hard to see, so change it. Type "workbench.colorCustomizations" in the search field and write the following items in settings.json.

```json
    "workbench.colorCustomizations": {
        "tab.activeBackground": "#0184bc"
    },
```

---

## Theme

### Visual Studio Code

* [Atom One Dark Theme](https://marketplace.visualstudio.com/items?itemName=akamud.vscode-theme-onedark)
* [Atom One Light Theme](https://marketplace.visualstudio.com/items?itemName=akamud.vscode-theme-onelight)
* [Helium Icon Theme](https://marketplace.visualstudio.com/items?itemName=jumpinjackie.vscode-map-preview)

### vim

* [shirotelin](https://github.com/yasukotelin/shirotelin)
* [One Half](https://github.com/sonph/onehalf)

---

# Procedure

## Key file conversion

Create a key converted from PuTTY format to Openssh format for use with ssh commands.

### Conversion method

1. Start [PuTTY Gen (PuTTY Key Generator)] from the start menu.
2. Load the PuTTY format key file with [File]-[Load private key].
3. Select [Conversions]-[Export OpenSSH key].
4. Do I have to protect it with a passphrase? A confirmation dialog box will be displayed. Select [Yes].
5. Enter the file name and save. For convenience, it is recommended that the extension of the original file name (* .ppk) is .pem.
6. Copy the generated key file under `~ / .ssh /`.
    * In case of Windows, if you put the key file other than under `~ /`, a connection error will occur.
    * For Linux, a connection error will occur unless you change the permissions so that only you can read and write after copying.
    ```sh
    chmod 600 ~/.ssh/*.pem
    ```

---

# setting file

## ~/.bashrc

* For Gitbash. Below is a copy of WSL's Ubuntu.
* For Windows, `C:\Users\[login user name]` is directly under the home directory (~/)

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
    PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\][GitBash] \u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\]\$ '
else
    PS1='${debian_chroot:+($debian_chroot)}[GitBash]: \u@\h:\w\$ '
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

Additional alias settings (Windows Git Bash)

```sh
alias cp='cp -i'
alias rm='rm -i'
alias mv='mv -i'
alias crontab='crontab -i'
alias vimdiff='vim -d'
alias view='vim -R'
alias curl='curl -s'
alias ssh='ssh -o ServerAliveInterval=60'
alias jq='jq -C'
alias cdh='cd ~/Documents'
alias cdd='cd ~/Downloads'
alias nostat="egrep -v '/(api/(status|doc)|bootstrap|jquery|ui|signin|public|health_check|HealthCheck::)'"
alias kubelog="kubectl stern -t "
alias kevent="kubectl get events --sort-by='.metadata.creationTimestamp' -A"
alias stern="kubectl-stern --timestamps "
alias aws_completer='/c/Program\ Files/Amazon/AWSCLIV2/aws_completer | 2lf'
alias mongo="mongosh"
#alias kp="kubectl get pods | s2u | 2lf"
#alias kd="kubectl get deploy | s2u | 2lf"
alias kt="kubectl top pods --sort-by=cpu | s2u | 2lf"
alias kcc="kubectl config current-context | s2u | 2lf"
alias tenki="curl https://wttr.in/Chiba"
alias awsmfa='aws-mfa --profile '
alias rehash='. ~/.bashrc'
alias addbom='nkf --overwrite --oc=UTF-8-BOM'
alias uft8conv='nkf --overwrite --oc=UTF-8 -Lu'
alias pwgen='wsl pwgen -y -n -c 16 1'
export LANG="ja_JP.utf8"

export LC_ALL=ja_JP.utf8
export LANG=ja_JP.utf8
export LANGUAGE=ja_JP.utf8
export LC_CTYPE="ja_JP.utf8"
export LC_NUMERIC="ja_JP.utf8"
export LC_TIME="ja_JP.utf8"
export LC_COLLATE="ja_JP.utf8"
export LC_MONETARY="ja_JP.utf8"
export LC_MESSAGES="ja_JP.utf8"
export GOPATH=/home/kabukawa/go
#source ~/.bash_completion.d/kubectl
source ~/.azure/az.completion
export MSYS=winsymlinks:nativestrict

HISTSIZE=1000
HISTFILESIZE=3000

function _compreply_ssh()
{
  COMPREPLY=(`cat ~/.ssh/config | grep -i -e '^host' | cut -d " " -f 2 | grep -E "$2"`)
}
complete -F _compreply_ssh ssh
function s2u ()
{
  iconv -f CP932 -t UTF-8 | tr -d '\r'
}
function u2s ()
{
  iconv -f UTF-8 -t CP932
}
function u2l ()
{
  if [ ${#1} -eq 10 ]; then
    date --date "@$1" +"%Y-%m-%d %H:%M:%S"
  elif [ ${#1} -ge 13 ]; then
    date --date "@${1:0:10}.${1:10:3}" +"%Y-%m-%d %H:%M:%S.%3N"
  fi
}
function l2u ()
{
  date +%s --date "$*"
}
function 2lf ()
{
  tr -d "\r"
}
function utc2jst ()
{ 
  date -d "${1} UTC" "+%Y/%m/%d %H:%M:%S"
}
function jst2utc ()
{ 
  TZ=UTC date -d "${1} JST"  "+%Y/%m/%d %H:%M:%S"
}
function gip ()
{
  curl ifconfig.io -4
  curl ifconfig.io -6
}
#alias tree='tree.com'
peco_search_history() 
{
  local l=$(HISTTIMEFORMAT= history | \
  sort -r | sed -E s/^\ *[0-9]\+\ \+// | \
  peco --query "$READLINE_LINE")
  READLINE_LINE="$l"
  READLINE_POINT=${#l}
}
bind -x '"\C-r": peco_search_history'
peco_cdr() 
{
  local l=$(CWDHISTORY= dirs -v | \
  sort -r | sed -E s/^\ *[0-9]\+\ \+// | \
  peco --query "$READLINE_LINE")
  READLINE_LINE="$l"
  READLINE_POINT=${#l}
  cd "$l"
}
alias cdr=peco_cdr
toppod() 
{
  kubectl top pod --use-protocol-buffers --no-headers | s2u | 2lf | \
		  sort -k3 -n -r | \
		  head -n 10
}
function ks() 
{
  kcontext=$(kubectl config get-contexts | s2u | 2lf | \
		  peco --initial-index=1 --prompt='kubectl config use-context > ' | \
		  sed -e 's/^\*//' | awk '{print $1}')
  clear
  if [ -n "$kcontext" ]; then
    kubectl config use-context $kcontext
  else
    kcc
  fi
}
function kp() 
{
  if [ -n "$1" ]; then
    kubectl get pods | s2u | 2lf | grep $1
  else
    kubectl get pods | s2u | 2lf
  fi
}
function kd() 
{
  if [ -n "$1" ]; then
    kubectl get deploy | s2u | 2lf | grep $1
  else
    kubectl get deploy | s2u | 2lf
  fi
}
function klogin ()
{
  klogin=$(kp | peco --initial-index=1 --prompt='pod login > ' | \
		  awk '{print $1}')
  clear
  if [ -n "$klogin" ]; then
    kubectl exec -it $klogin -- //bin/bash
  fi
}
function distlogin() 
{
  dcontext=$(wsl --list --quiet | s2u  | \
		  peco --initial-index=0 --prompt='Distribution > ' | \
		  awk '{print $1}')
  clear
  if [ -n "$dcontext" ]; then
    wsl --distribution $dcontext --cd "~"
  fi
}
function ass() 
{
	acontext=$(az account list --query \
			'[?tenantId==`754dd7c9-3d26-46fc-a8cc-91e046d26e1d`].[id, name]' -o tsv | \
			s2u | sed -e 's/スポンサー プラン/Sponsor Plans/g' | \
			peco --initial-index=0 --prompt='Subscriptuon > ' | awk '{print $1}')
	clear
	if [ -n "$acontext" ]; then
      az account set -s "$acontext"
	fi
	az account show --query "name" -o tsv
}
function pod-restart() 
{
  local DEPLOYLIST=`kubectl get deploy`
  rcontext=$(echo "${DEPLOYLIST}" | \
		  peco --initial-index=1 --prompt='kubectl get pods > ' | \
		  awk '{print $1}')
  clear
  if [ -n "$rcontext" ]; then
    kubectl rollout restart deployment/$rcontext
  fi
}
function sql() 
{
  mcontext=$(ls ~/.mysql/* | \
		  sed -e 's/.*\///g' | \
		  peco --initial-index=0 --prompt='mysql > ' | \
		  awk '{print $1}')
  clear
  if [ -n "$mcontext" ]; then
    mysql --defaults-file=~/.mysql/$mcontext
  fi
}
function vpn() 
{
  vcontext=$(ls -a  ~/.vpn/* | \
		  sed -e 's/.*\///g' | \
		  peco --initial-index=0 --prompt='vpn > ' | \
		  awk '{print $1}')
  clear
  if [ -n "$vcontext" ]; then
	rasdial `cat ~/.vpn/$vcontext` | egrep -v '(コマンドは正常に|Binary file)'
  fi
}
function mg() 
{
  gcontext=$(ls -a  ~/.mongo/* | \
		  sed -e 's/.*\///g' | \
		  peco --initial-index=0 --prompt='mongo > ' | \
		  awk '{print $1}')
  clear
  if [ -n "$gcontext" ]; then
	mongo `cat ~/.mongo/$gcontext`
  fi
}
function _compreply_awsprofile()
{
  COMPREPLY=(`cat ~/.aws/config | \
		  grep -i -e '^\[' | \
		  sed -e 's/\[//g' -e 's/\]//g' | \
		  cut -d " " -f 2 | grep -E "$2"`)
}
complete -F _compreply_awsprofile awsmfa
function awsssm()
{
  local INSTANCES=`awsec2 ${1}`
  SSM_TARGET_HOST=$(echo "${INSTANCES}" | \
      peco --initial-index=0 --prompt='ssm > ' | \
      awk '{print $1}')
  if [ -n "${SSM_TARGET_HOST}" ]; then
    chcp.com 65001
    aws ssm start-session --profile ${1} --target ${SSM_TARGET_HOST}
    chcp.com 932
  fi
}
complete -F _compreply_awsprofile awsssm
function awspfrds()
{
  local INSTANCES=`awsec2 ${1}`
  SSM_TARGET_HOST=$(echo "${INSTANCES}" | \
		  peco --initial-index=0 --prompt='ssm > ' | \
		  awk '{print $1}')
  local DBINSTANCES=`awsrds ${1}`
  RDS_TARGET_HOST=$(echo "${DBINSTANCES}" | \
		  peco --initial-index=0 --prompt='ssm > ' | \
		  awk '{print $1}')
  if [ -n "${SSM_TARGET_HOST}" ]; then
    aws ssm start-session --profile ${1} --target ${SSM_TARGET_HOST} \
          --cli-read-timeout 0 \
          --cli-connect-timeout 0 \
          --document-name AWS-StartPortForwardingSessionToRemoteHost \
		  --parameters "{\"host\":[\"${RDS_TARGET_HOST}\"],\"portNumber\":[\"3306\"], \"localPortNumber\":[\"13306\"]}"
  fi
}
complete -F _compreply_awsprofile awspfrds
function awslogtail()
{
  local LOGGROUPS=`awsloggroups ${1}`
  TARGET_LOGGROUP=$(echo "${LOGGROUPS}" | \
		  peco --initial-index=0 --prompt='log grpups > ' | \
		  awk '{print $1}')
  if [ -n "${TARGET_LOGGROUP}" ]; then
    aws logs --profile ${1} tail --format short --since 60m --follow ${TARGET_LOGGROUP}
  fi
}
complete -F _compreply_awsprofile awslogtail
function awsec2 () 
{
  aws ec2 describe-instances \
  --profile ${1} \
  --query 'Reservations[].Instances[].{ID:InstanceId, Name:Tags[?Key==`Name`] | [0].Value, State:State.Name}' \
  --output text | column -t
}
complete -F _compreply_awsprofile awsec2
function awsrds () 
{
  aws rds describe-db-instances \
  --profile ${1} \
  --query 'DBInstances[].{ID:DBInstanceIdentifier, Class:DBInstanceClass, Address:Endpoint.Address, Name:TagList[?Key==`Name`] | [0].Value, State:DBInstanceStatus}' \
  --output text | column -t
}
complete -F _compreply_awsprofile awsrds
function awssecrets () 
{
  for NAME in `aws secretsmanager list-secrets \
		  --profile ${1} \
		  --query "SecretList[].Name" \
		  --output text | 2lf`; 
  do
    echo ${NAME}
	aws secretsmanager get-secret-value \
			--profile ${1} \
			--secret-id ${NAME} | \
			jq -r ".SecretString" | jq ; 
  done
}
complete -F _compreply_awsprofile awssecrets
function awsloggroups () 
{
  aws logs describe-log-groups\
  --profile ${1} \
  --query 'logGroups[].logGroupName' \
  --output text | sed -e 's/\t/\n/g' | grep ^dxp | grep ecm
}
complete -F _compreply_awsprofile awsloggroups
function ecs_info ()
{
  CLUSTOR=`aws ecs \
    --profile ${1} list-clusters | \
    jq -r .clusterArns[] | grep ecm`

  TASK_ID_LIST=`aws ecs --profile ${1} list-tasks \
    --cluster ${CLUSTOR} \
    --query "taskArns" \
    --output text`

  for TASK_ID_ARN in ${TASK_ID_LIST}
  do
    TASK_ID=`echo "${TASK_ID_ARN}" | sed -e 's/.*\///'`
    CONTAINER=`aws ecs --profile ${1} describe-tasks \
      --cluster ${CLUSTOR} \
      --tasks ${TASK_ID} \
      --query 'tasks[].containers[].name' \
	  --output text`
    printf "%s\t%s\t%s\n" ${TASK_ID} ${CONTAINER} ${CLUSTOR}
  done
}
function ecslogin()
{
  local TASKLIST=`ecs_info ${1}`
  TASK_INFOS=$(echo "${TASKLIST}" | \
		  peco --initial-index=0 --prompt='ecs tasks > ' | \
		  awk '{print $0}')
  if [ -n "${TASK_INFOS}" ]; then
    #aws logs --profile ${1} tail --format short --since 60m --follow ${TARGET_LOGGROUP}
	clear
	CLUSTOR=`echo ${TASK_INFOS} | cut -f3 -d' '`
	TASK_ID=`echo ${TASK_INFOS} | cut -f1 -d' '`
	CONTAINER=`echo ${TASK_INFOS} | cut -f2 -d' '`
	aws ecs execute-command \
      --profile ${1} \
      --cluster ${CLUSTOR} \
      --task ${TASK_ID} \
      --container ${CONTAINER} \
      --interactive \
      --command "//bin/bash"

  fi
}
complete -F _compreply_awsprofile ecslogin

function dockerip() 
{
  dcontext=$(docker ps | grep -v CONTAINER | sed -e 's/  */ /g' | cut -f1,2 -d" " | \
		  peco --initial-index=0 --prompt='container > ' | \
		  awk '{print $1}')
  #clear
  if [ -n "$dcontext" ]; then
    docker inspect $dcontext | grep IPAddress
  fi
}

complete -C aws_completer aws
source <(kubectl completion bash)
```

## ~/.gitconfig (Windows)

* For Windows, `C:\Users\[login user name]` is directly under the home directory (~/)
* Replace {username} and {email address} with your own.

```ini
[user]
    name = {username}
    email = {email address}
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

* Replace {username} and {email address} with your own.

```ini
[user]
    name = {username}
    email = {email address}
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

* For Windows, `C:\Users\[login user name]` is directly under the home directory (~ /)

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

#Color
#If orange turns red, screen may not support 256 colors
# FYI: https://qiita.com/trapple/items/8ad1b0a7c4fa5b8341b0
# $ brew tap homebrew/dupes
# $ brew install screen
defbce on
term xterm-256color


# Status line
hardstatus alwayslastline "%{= cd} %-w%{= wk} %n %t* %{-}%+w %= LoadAVG [%l] "

# Escape key
#escape ^Tt

#Mouse scroll
termcapinfo xterm* ti@:te@

# Number of scroll lines
defscrollback 10000

#Clear buffers such as vim, less and tig at the end
altscreen on

#Default shell
shell $SHELL
```

## ~/.ssh/config

* For Windows, `C:\Users\[login user name]` is directly under the home directory (~/)
* For Linux, change the permissions under `~/.ssh/` so that only you can read and write.
* Replace {username} and {keyfilename} with your own.

```sh
## develop
Host {host name}
  HostName {IP address}
  User {user name}
  IdentityFile ~/.ssh/{key file name}
```

* If you want to prompt the environment name after login

```sh
## develop
Host {host name}
  HostName {IP address}
  User {user name}
  IdentityFile ~/.ssh/{key file name}
  RequestTTY yes
  RemoteCommand PS1="\[\e[1;32m\][\u@\h \w] [environment name] $ \[\e[m\]" bash --login
```

## ~/.my.cnf

```ini
[client]
host={hostname}
user={username}
password={password}
port=3306
database={schema name}
```