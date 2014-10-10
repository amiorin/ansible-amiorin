## Intro
Using linux without my dotfiles is annoying.
This playbook fixes this. It copies my settings for vim, zsh and other programs from my osx MBP to the linux machine
and it uses ``linuxbrew`` to install new software.

## Requirements
* ansible
* vagrant
* virtualbox
* root access to the target machine (I'm working to make it optional)

```sh
1GB of ram for compiling the_silver_searcher
```

## Instructions
```sh
sudo easy_install pip
sudo pip install ansible
vagrant up
ansible-playbook site.yml

# if you change a dotfile
ansible-playbook site.yml --tags dotfiles
```

## Fork
It will not work out of the box on your MBP. You need to customize/fix it.

## Previous work
* dotfiles in git/dropbox. It didn't work for me.
* NIS/Yellow pages feature mount home on login. ;-)


## Problems with osx
These are notes about osx mavericks fresh installations.

* ``/usr/bin/zsh`` breaks ``sudo -s`` (very slow after pressing enter)

```
mv /usr/bin/git /usr/bin/git.original
```

* root uses ``/usr/bin/vi`` and is too old compared to macvim

```
cd /usr/bin
ln -sf /usr/local/bin/vi .
```
