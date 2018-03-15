![OS](https://img.shields.io/badge/OS-Ubuntu%2016.4-orange.svg)  ![Language](https://img.shields.io/badge/Language-C%23-red.svg)

# Install [Visual Studio Code](https://code.visualstudio.com/)

There few ways, you can choose:

1. 
```Shell
  sudo add-apt-repository ppa:ubuntu-desktop/ubuntu-make
  sudo apt-get update && sudo apt-get install ubuntu-make
  umake web visual-studio-code
```
2. Install and start deb from official [page](https://code.visualstudio.com/Download)
3. Install deb from official [page](https://code.visualstudio.com/Download) and start it from CLI with *sudo dpkg -i DEB_PACKAGE* command

# Install *docker*

You can find all information [here](https://docs.microsoft.com/ru-ru/dotnet/core/linux-prerequisites?tabs=netcore2x)
```Shell
> curl https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > microsoft.gpg
> sudo mv microsoft.gpg /etc/apt/trusted.gpg.d/microsoft.gpg
> sudo sh -c 'echo "deb [arch=amd64] https://packages.microsoft.com/repos/microsoft-ubuntu-xenial-prod xenial main" > /etc/apt/sources.list.d/dotnetdev.list'
> sudo apt-get update
> sudo apt-get install dotnet-sdk-2.1.4
> dotnet --version #!check results
```

# Install and setup *Git*

Generate keys:
```Shell
> ssh-keygen -C "tfs@mail.com" #!your tfs email here
Generating public/private rsa key pair.
Enter file in which to save the key (/home/frank/.ssh/id_rsa): /home/frank/.ssh/id_rsa
Enter passphrase (empty for no passphrase): passphrase
Enter same passphrase again: passphrase
Your identification has been saved in /home/frank/.ssh/id_rsa.
Your public key has been saved in /home/frank/.ssh/id_rsa.pub.
 ```
 
Copy the content of your public SSH key, it is the file id_rsa.pub by default:
Paste the content into your *GitHub*/*BitBucket* account on the SSH key section or past if to *Tfs git repo* like [here](https://docs.microsoft.com/en-us/vsts/git/use-ssh-keys-to-authenticate)

Add private key to ssh: 
```Shell
> ssh-add ~/.ssh/<private>
```

# Clone repo
```Shell
GitHub: git clone git@github.com:YOUR_USERNAME/REPO_NAME.git
BitBucket: git clone git@bitbucket.org:USERNAME/REPO_NAME.git
TFS: git clone ssh://tfs.<xxx>.net:22/DefaultCollection/REPO_NAME
```

# Git clients for linux:
* https://www.gitkraken.com/
* git-gui

# Additional
| #	|	|
|-|-|
|Check Ubuntu version|lsb_release -r|
