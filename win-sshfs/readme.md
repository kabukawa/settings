# win-sshfs

How to use win-sshfs to use Windows like a network drive.
If you have an older OS, you cannot use VS Code's Remote SSH, so this is a workaround.
It's easy to use, but it's also easy to break, so please use it with the latest care.

## Setup

## Installation

Install the following two files.

* [Dokany](https://github.com/dokan-dev/dokany/releases/download/v1.0.0/DokanSetup-1.0.0.5000.exe)
* [WinSSHFS](https://github.com/feo-cz/win-sshfs/releases/download/1.6.1/WinSSHFS-1.6.1.13-devel.msi)

## Startup.

Search for win-sshfs in the start menu and start it.

### Settings. 1.

1. right mouse click on the icon (yellow icon). 2.
2. select "Show Manager" to open the configuration window. 3.
Click the Add button at the bottom left of the dialog. 4.
Enter information such as ssh login to the host.
The following is an example of mounting the remote server hogehoge-dev on drive G.
    * DriveName: {any name}
    * Host: {host name or IP address of hogehoge-dev}
    * Port: 22
    * Username: {User who will login to hogehoge-dev via ssh}
    * Password: {password of the user who will log in to hogehoge-dev}
    * Directory: {path you want to mount}
    * DriveLetter: G
    * Mount at Login: unchecked (basically, mount only when you use it) 5.
5. click on the Save button to save.

### Mount

When you click the Mount button, the path specified in `Directory` of `Host` will be mounted as the `DriveLetter` drive.
The rest is the same as using it on Windows. You can also copy and edit the drive in Explorer.

### Unmount

When you are done using it, unmount it.