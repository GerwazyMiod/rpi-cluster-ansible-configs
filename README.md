# rpi-cluster-ansible-configs
Ansible roles and playbooks for Raspberry pi cluster

Inspired by: 
* https://github.com/chesterbr/chester-ansible-configs
* https://github.com/cloudalchemy/ansible-node-exporter

Use provisioning.yml playbook like this:
```bash
ansible-playbook -i hosts provisioning.yml -k
ansible-playbook -i hosts cluster.yml 
```

After playing everything from Ansible - log into your server node and run:
```bash
$ sudo k3s kubectl get node -o wide
```
You should see all of your nodes broadcasting a _Ready_ status.


### What is configured here? ###

Raspberry cluster consists of 5 nodes:
* master node (node 1)
* worker node (all nodes including node 1)

#### Master Node ####

#### Worker Node ####
Installed debian packages:
* git
* go (golang)

Other packages:
* Node exporter ( https://github.com/prometheus/node_exporter )

#### Basic setup for every Raspberry Pi ####
User: exec, with ssh public key \
Timezone: Warsaw/Poland
