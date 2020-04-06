# Set Up Homebridge on Docker on Raspbian

## Prep

```bash
passwd
mkdir $HOME/.ssh
ssh-keygen -t rsa -f $HOME/.ssh/id_rsa
ssh-agent > $HOME/.ssh/agentrc
source $HOME/.ssh/agentrc
ssh-add $HOME/.ssh/id_rsa
```

Install

- [x] zsh
    sudo apt-get update && sudo apt-get install -y zsh
- [x] dotfiles
    git clone git@github.com:/clhynfield/dotfiles.git
    # follow README
- [x] direnv
- [x] antibody
- [x] tmux
- [x] mosh


## Install Docker

From [Get Docker Engine - Community for Debian](https://docs.docker.com/install/linux/docker-ce/debian/#install-using-the-convenience-script):

```bash
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
```

Allow `pi` user to use Docker

```bash
sudo usermod -aG docker pi
```
