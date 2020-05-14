# ansible-desktop-ubuntu-18.04

Personal Ansible playbook to bootstrap a desktop setup with Ubuntu 18.04

## Setup

```sh
sudo apt update && sudo apt install -y ansible git
```

## Clone

```sh
git clone git://github.com/panagiks/ansible-desktop-ubuntu-18.04 && cd ansible-desktop-ubuntu-18.04
```

## Install dependencies

```sh
ansible-galaxy install -r requirements.txt
```

## Run the playbook

```sh
ansible-playbook --ask-become-pass playbook.yml
```

## Logout from the user session

Since some configuration is placed in `.profile` a session (not terminal) logout is requeired.

## Verify functionality

