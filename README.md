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

## Configure appearance

- Open `Settings > Apparance` and:
  - select `Dark` under `Window colors`
  - Enable `Auto-hide the Dock`
  - Set `Icon size` to `28` (or adjust at will)
  - Set `Position on screen` to `Bottom` (or adjust at will)
- Open `Startup Applications Preferences`
  - Select `Add`
  - Add a descriptive name (for Caffeine Indicator)
  - Select `Browse...` navigate to `/bin` (by clicking `+ Other Locations`) and select `caffeine-indicator` from the list
- Open `Terminal` and go to `Preferences`
  - In `General` set `Theme variant` to `Dark`
  - In `Profiles`:
    - Set `Cursor shape` to `Underline`
    - Set `Curson blinking` to `Enabled`
    - Disable `Terminal bell`
    - Under `Colors > Text and Background color > Built-in schemes` select `Solarized dark`
    - Under `Colors > Palette > Built-in schemes` select `Solarized`

## Logout from the user session

Since some configuration is placed in `.profile` a session (not terminal) logout is requeired.

## Verify functionality

