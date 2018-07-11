# Ansible for Rails on Ubuntu Desktop 16.04

**WARNING:** Do NOT use this script to build production environments!

## Download Ubuntu ISO

http://releases.ubuntu.com/releases/16.04/ubuntu-16.04.4-desktop-amd64.iso

Use the ISO to create a VM with VirtualBox (i.e. Install Ubuntu as a VM)

## Install dependencies

```
sudo apt-add-repository -y ppa:ansible/ansible
sudo apt-get update
sudo apt-get -y install virtualbox-guest-dkms ansible git vim
```

## Clone repository

```
git clone git@github.com:npearson72/ansible-for-rails-on-ubuntu-desktop.git
cd ansible-for-rails-on-ubuntu-desktop
```

## Prepare variables

Fill out missing values in the `.env` file:

`cp .env.example .env`

## Execute Ansible playbook

`sh -ac ". ./.env && ansible-playbook main.yml -i inventory -v -K"`

## Reboot to be safe

`sudo reboot`
