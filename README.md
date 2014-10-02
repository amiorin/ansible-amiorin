## Intro
Fresh installation of linux are unusable in my opinion.
This playbook fix this. It copies my settings for vim, zsh and other programs from my osx MBP to the linux machine.

## Requirements
* ansible
* vagrant
* virtualbox

## Instructions
```sh
sudo easy_install pip
sudo pip install ansible
vagrant up
ansible-playbook site.yml
```

## Fork
It will not work out of the box on your MBP. You need to customize/fix it.

## Previous work
NIS/Yellow pages feature mount home on login. ;-)

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
