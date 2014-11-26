# Intro

Small [Ansible](https://github.com/ansible/ansible) role that changes bashrc file to provide a log of everything that is typed, by any user.

# Where is the log?

After this role is executed, and a user logs for the first time, in the user's home there will be a file `.commands.log`. (This also applies for the root user!)

## How to understand the log file

The log file is basically a csv with the following fields:

```
date,hour,user@machine:location,command
```

Example:

```
2014-11-26,19:12:14,vagrant@vagrant-ubuntu-utopic-64:/home/vagrant,ls
```

# Testing

For basic testing, do the following steps:

1. `vagrant up`
1. `ansible-playbook command_logger.yml`
