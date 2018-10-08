# Ansible Playbook for Personal Dev Box Config

** Fork from daveyb's Ansible Playbook

This is my personal (and always a WIP, beware the monsters) Ansible playbook for setting up and enforcing a consistent config on my computers.

Out-of-the-box, the plays will run on `localhost`, but it can be configured to run on remote *nix machines as well.

It's designed to init new dotfiles as needed, so be aware that it may clobber existing dotfiles you already have.

## Usage

### Prerequisites
1. Python 2.7+ and `pip`
2. A user account that's a member of the sudoers group `adduser <user> sudo`
3. Ansible `sudo pip install ansible`
4. An internet connection

### Run all plays
`ansible-playbook -i hosts main.yml --ask-become-pass`

### Run a specific play based on tag (optional)
`ansible-playbook -i hosts main.yml --ask-become-pass -t zsh`
