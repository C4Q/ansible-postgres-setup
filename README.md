# Install and setup Postgres on an ubuntu linux Digital Ocean machine using ansible.

This is intended for a fresh Ubuntu droplet.

## Prerequisites

These are prerequisites for your *local* development machine.

Install pip:

```bash
sudo easy_install pip
```

And these python dependencies:

```bash
sudo pip install paramiko PyYAML Jinja2 httplib2
```

Now we can install ansible locally:

```bash
cd ansible-code
git clone git://github.com/ansible/ansible.git --recursive
```
Then checkout the latest version (tag)
https://github.com/ansible/ansible/releases
or run `git tag`.
```bash
cd ./ansible
git checkout v1.8.1
source ./hacking/env-setup
cd ..
```

The script on the last line adds `ansible` and `ansible-playbook` to your path.

### Update ansible_hosts file

Now you can setup the machine using ansible:

You'll need to change the connection parameters in the file `ansible_hosts`.

Change the IP address, username, and private key location to the appropriate values.


# Run the installation
```bash
ansible-playbook main.yml
```
