# win-sshfs

win-sshfsを使ってWindowsのネットワークドライブ的に使えるようにする方法。
OSが古いとVS CodeのRemote SSHが使えないので、その回避策。
使いやすくなる分、壊したりもしやすくなるので、使う場合は最新の注意を払って使ってください。

## セットアップ

### インストール

以下の2つをインストール。

* [Dokany](https://github.com/dokan-dev/dokany/releases/download/v1.0.0/DokanSetup-1.0.0.5000.exe)
* [WinSSHFS](https://github.com/feo-cz/win-sshfs/releases/download/1.6.1/WinSSHFS-1.6.1.13-devel.msi)

### 起動

スタートメニューからwin-sshfsを検索して起動

### 設定

1. 起動したらタスクトレイに常駐(黄色いアイコンのやつ)するので、アイコン上でマウス右クリック
2. Show Managerを選択して設定画面を開く
3. ダイアログの左下に有る Add ボタンをクリック
4. ホストへのsshでのログインなどの情報を入力
以下はリモートサーバー hogehoge-dev をGドライブにマウントする例
    * DriveName：{任意の名前}
    * Host：{hogehoge-dev のホスト名もしくはIPアドレス}
    * Port：22
    * Username：{hogehoge-dev にsshログインするユーザー}
    * Password：{hogehoge-dev にsshログインするユーザーのパスワード}
    * Directory：{マウントしたいパス}
    * DriveLetter：G
    * Mount at Login：チェックを外す(基本的には使うときだけマウントする)
5. Save ボタンをクリックして保存

### マウント

Mount ボタンを押すと `Host` の `Directory`で指定したパスが `DriveLetter` ドライブとしてマウントされる。
あとはWindows上で使うのと同じ。エクスプローラ上でコピーしたり編集操作も可能

### アンマウント

使い終わったらunmountしておく。Kv