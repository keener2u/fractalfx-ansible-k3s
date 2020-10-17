# fractalfx-ansible-k3s
Playbook for building a HA k3s cluster with Embedded ETCD for Rancher in Linode cloud
How-to
-install Ansible > 2.7
-pip install linode_api4
-ansible-galaxy collection install community.general
-change /group_vars/k3s_group/vars to include vault password and token for your setup
-run ansible-playbook linode_create.yml



Creates three Lindodes
Todo:
Secures and turns on the firewall
Secures SSHD to only accept pub/priv key
sets hostname
Opens up the ports for k3s
installs k3sup
install helm
installs ca-cert
installs rancher
