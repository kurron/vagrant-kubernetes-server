# Overview
This project is a Vagrant box that is provisioned for Kubernetes development.

# Prerequisites

* [Vagrant](https://www.vagrantup.com/) installed and working
* [VirtualBox](https://www.virtualbox.org/) installed and working

# Building
All the components of the environment live in repositories on the internet so there is nothing to build.

# Installation
Type `vagrant up` and wait a few moments. The construction time of the box depends on your internet speeds.

## Upgrading
Sometimes the Vagrant file changes which can cause some subtle issues, such as creating an orphaned virutal machine.
The safest upgrade procedure is the following:

1. `vagrant destroy` to remove the existing box
1. `git pull` to download the new files
1. **`vagrant box outdated`** to see if newer version of the box is available
1. `vagrant box update --box <boxname>` to pull down the current version of the box
1. `vagrant up` to build the new box

# Tips and Tricks

## RAM and CPU Settings
If you examine the `vagrantfile` file, you will see how the virtual machine is configured.
Feel free to change these values to match your computer's hardware.

## Verifying The Setup
Log into the system with a username of `vagrant` and password of `vagrant`.

## Check Components 
The K8s components can take a while to fully come up. Use `watch juju status`
to monitor things until everything is active.

# Troubleshooting

## Partial Failure

# License and Credits
This project is licensed under the [Apache License Version 2.0, January 2004](http://www.apache.org/licenses/).
