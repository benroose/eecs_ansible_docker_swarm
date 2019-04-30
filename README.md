# Docker Swarm Testing Cluster

### Ansible deployment - under development

## Description

The architecture for the docker swarm testing cluster will be:

     -----------------------------       ----------------------------
    |  swarm-manager-[00-03]      | --- |  swarm-worker-[00-06]      |
    |  Private IP                 |     |  Private IP                |
     -----------------------------       ----------------------------
                      \                            /
                    -----------------------------------
                   |  dm-host (docker-machine/libvirt) |
                   |  Public IP + Private vrouter      |
                    -----------------------------------

DEVELOPMENT ONLY - DO NOT USE FOR PRODUCTION ENVIRONMENTS

This is a set of Ansible playbooks to provision a docker swarm cluster built on docker-machine with libvirt (KVM) for running on RHEL or CentOS. Due to limitations with Ansible's docker-machine dynamic inventory,these playbooks should be run on a locally accessible host (not remote).

## Provisioning Notes

## Prerequisites

Before you can run any of these playbooks, you will need to [install Ansible](http://docs.ansible.com/intro_installation.html), and run the following command to download dependencies (from within the same directory as this README file):

    $ ansible-galaxy install -r requirements.yml

## Configure the host server

Pre-suppositions: A locally accessible user on the development/testing host must be created and added to both "wheel" and "libvirt" groups.

TBC

## Provision and configure the docker swarm nodes

To provision the virtual instances and configure them using Ansible, follow these steps (from within this directory):

TBC

### Ancillary Notes

  - Private network IP addresses for virtual machines within the docker-machine host are used for all cross-instance communication. It is assumed the private network is secure.

## About the Author

This project was created by Ben Roose for use at Wichita State University.
