[![Python](https://img.shields.io/badge/bash-5.0.17(1)-blue)](https://pypi.python.org/pypi/azure-devops)

# [~/.bashrc](./.bashrc)
My `~/.bashrc` configurations. It includes npm autocompletion, python virtualenv wrappers, git aliases, and more!
# 🚀 Useful tools

Installation steps for tools I download in almost every dev environment

## [pyenv](https://github.com/pyenv/pyenv) and [pyenv-virtualenv](https://github.com/pyenv/pyenv-virtualenv)

Great for managing multiple versions of python on the same machine

```bash
curl https://pyenv.run | bash
```

Update `~/.bashrc` with pyenv and pyenv-virtualenv references

```bash
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
echo 'command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
echo 'eval "$(pyenv init -)"' >> ~/.bashrc
```

```bash
eval "$(pyenv virtualenv-init -)"
```

```bash
pyenv install 3.11
pyenv virtualenv 3.10 my-virtualenv-3.10
pyenv version
pyenv activate my-virtualenv-3.10
```

## [virtualenv](https://virtualenv.pypa.io/en/latest/installation.html)
```bash
sudo apt install python3-virtualenv
```
## [virtualenvwrapper](https://virtualenvwrapper.readthedocs.io/en/latest/)

Assumes python3 and pip3 installed.

```bash
pip3 install --user virtualenvwrapper
```
```bash
# Run in shell after installer OR Add this to ~/.bashrc
export WORKON_HOME=~/.virtualenvs
export VIRTUALENVWRAPPER_PYTHON=/usr/bin/python3
export VIRTUALENVWRAPPER_VIRTUALENV=/usr/bin/virtualenv
mkdir -p $WORKON_HOME
. /home/$USER/.local/bin/virtualenvwrapper.sh
# Alternatively,
# export VIRTUALENVWRAPPER_VIRTUALENV=/home/$USER/.local/bin/virtualenv
export CLOUDSDK_PYTHON=/usr/bin/python2
```

## [jq](https://stedolan.github.io/jq/)
```bash
sudo apt-get install jq
```

## [postgresql](https://www.postgresql.org/download/linux/ubuntu/)
```bash
# Create the file repository configuration:
sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list'

# Import the repository signing key:
wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -

# Update the package lists:
sudo apt-get update

# Install the latest version of PostgreSQL.
# If you want a specific version, use 'postgresql-12' or similar instead of 'postgresql':
sudo apt-get -y install postgresql
``` 

## [peek](https://github.com/phw/peek)

```bash
sudo add-apt-repository ppa:peek-developers/stable
sudo apt update
sudo apt install peek
```

## [shutter](https://shutter-project.org/downloads/third-party-packages/)
```bash
sudo apt install shutter
```

## [vscode](https://code.visualstudio.com/docs/?dv=linux64_deb)

## [git secret](https://git-secret.io/)
```bash
sudo sh -c "echo 'deb https://gitsecret.jfrog.io/artifactory/git-secret-deb git-secret main' >> /etc/apt/sources.list"
wget -qO - 'https://gitsecret.jfrog.io/artifactory/api/gpg/key/public' | sudo apt-key add -
sudo apt-get update && sudo apt-get install -y git-secret
```
## [net-tools](https://installati.one/ubuntu/20.04/net-tools/)
```bash
sudo apt-get update && sudo apt-get -y install net-tools
ifconfig
```

## [docker](https://docs.docker.com/engine/install/ubuntu/)
```bash
sudo apt-get update
sudo apt-get install ca-certificates curl gnupg lsb-release
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

echo \
"deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
$(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin
```

## [curl](https://www.cyberciti.biz/faq/how-to-install-curl-command-on-a-ubuntu-linux/)
```
sudo apt install curl
```

## [vim]()
```bash
sudo apt install vim
```

## [go](https://go.dev/doc/install)
```bash
rm -rf /usr/local/go && tar -C /usr/local -xzf go1.18.3.linux-amd64.tar.gz
go version
```

## [nvm](https://github.com/nvm-sh/nvm)
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
```

## [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
```bash
sudo apt install git-all
```

## [ssh client/server](https://www.cyberciti.biz/faq/ubuntu-linux-install-openssh-server/)
```bash
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install openssh-client openssh-server
sudo systemctl enable ssh
sudo systemctl start ssh
sudo ufw allow ssh
```
## [wget]()
```bash
sudo apt install wget
```

## [yq](https://github.com/mikefarah/yq)
```bash
VERSION=v4.2.0
BINARY=yq_linux_amd64
wget https://github.com/mikefarah/yq/releases/download/${VERSION}/${BINARY}.tar.gz -O - |\
  tar xz && mv ${BINARY} /usr/bin/yq
```

## [kubernetes - kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/)
```bash
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl
```

## [kubernetes - kind](https://kind.sigs.k8s.io/docs/user/quick-start/)
```
curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.14.0/kind-linux-amd64
chmod +x ./kind
mv ./kind /ur/localbin/kind
```

## [wait-for-it](https://github.com/vishnubob/wait-for-it)
```bash
sudo apt install wait-for-it
```
## [~/.psqlrc](./.psqlrc)

## [~/.tmux.conf](./.tmux.conf)

