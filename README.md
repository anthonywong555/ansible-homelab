# ansible-homelab

Resources:
- [How to Use Ansible to Install and Set Up Docker on Ubuntu 20.04](https://www.digitalocean.com/community/tutorials/how-to-use-ansible-to-install-and-set-up-docker-on-ubuntu-20-04)

Notes for Unraid with Ubuntu 24.04.1

When ssh into the Ubuntu VM, it's possible that the ssh service is not installed / enabled. To fix that, do the following:

```sh
sudo apt update
sudo apt install openssh-server
sudo systemctl enable ssh
sudo systemctl start ssh
```

Once you do that, you can get the IP address of the VM:

```sh
ip a
```

To run the playbook, execute the following command:
```sh
ansible-playbook tasks/asdf-plugin.yml -l vm1 -u anthony -K
```