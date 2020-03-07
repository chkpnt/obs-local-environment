Using [Vagrant](https://www.vagrantup.com/) and [Ansible](https://github.com/ansible/ansible) to set up a VM as a local enviroment for the [openSUSE Build Service](https://build.opensuse.org/).

# Prerequisites
Only VirtualBox, Vagrant and Ansible are required. On macOS, these dependencies can be installed using Homebrew:

```
$ brew cask install virtualbox
$ brew cask install vagrant
$ brew install ansible
```

For managing your Vagrant virtual machines, I can recommend the use of [Vagrant-Manager](http://vagrantmanager.com/), a small utility app for the menu bar.

```
$ brew cask install vagrant-manager
```

# Configuration
The credentials needed to access https://build.opensuse.org have to be configured in `provisioning/credentials.yml`.

# Basic commands
Starts the virtual machine:
```
$ vagrant up
```

(Re-)runs the Ansible playbook:
```
$ vagrant provision
```

Access the virtual machine via ssh:
```
$ vagrant ssh
```