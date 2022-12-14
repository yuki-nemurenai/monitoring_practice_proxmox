# Slurm DevOps Upgrade: Monitoring and Logging practice (deploy to ProxmoxVE Cluster)
### Contains roles:
```
- Proxmox: Generate SSH Keypair and Create container with SSH key
- Prometheus
- Node Exporter
- Elasticsearch
- Kibana
- Fluentbit
```
### Variables used for the container creating ***proxmox/defaults/main.yml***:
```
vmid: <value>
node: <name>
api_user: <username@pam>
api_password: <user_password>
api_host: <ip>
password: <ct_password>
hostname: <hostname>
ostemplate: <'storage:ct_image'>
description: <created with ansible>
netif: <'net, gw, ip, bridge name'>
storage: <"storage_name">
disk: <value_gb>
cores: <value_cores>
memory: <value_mb>
```
### Don't forget to change variables in the host.ini file

### Run playbook
```
ansible-playbook main_playbook.yml
```
### Notes:
```
- keys\rsa4096_key is the ssh_key_generate.yml playbook's running example
- example Proxmox Variables: proxmox/defaults/main.yml
- Kibana and Elastic repo replaced: 'deb [trusted=yes] https://mirror.yandex.ru/mirrors/elastic/7/ stable main'
```
