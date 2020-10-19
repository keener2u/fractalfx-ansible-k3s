# fractalfx-ansible-k3s
Playbook for building a HA k3s cluster with Embedded ETCD for Rancher in Linode cloud
How-to
-install Ansible > 2.7
-pip install linode_api4
-ansible-galaxy collection install community.general
-change /group_vars/k3s_group/vars to include vault password and token for your setup
-setup an session key enviornment variable
--export LINODE_ACCESS_TOKEN=$(cat /home/keener2u/.ssh/token)
-make sure you turn on ssh-agent and add your key 
-run ansible-playbook -i linode.yml main.yml



Creates three Lindodes
Secures and turns on the firewall
Opens up the ports for k3s distributed etcd
sets hostname
installs k3sup
initializes first server with --cluster
initilies node 2-n as --server


Todo:
Secures SSHD to only accept pub/priv key
add in handlers to wait until linodes are built before proceeding
install helm
installs ca-cert
installs rancher
