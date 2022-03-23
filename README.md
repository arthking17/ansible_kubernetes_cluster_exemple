# cluster_kubernetes

Automation of Kubernetes cluster creation


## Get started with creation of Kubernetes cluster using Ansible 🛠️⚙️💡

## share ssh-key to all hosts to configure

```
$ ssh-keygen #on all host where you want to connect via ssh 
$ ssh-copy-id username@ip-addr #ip-addr of host where you generate ssh key
```

## create vault password

- [ ] generate the encrypt_value in terminal before copy it
```
$ ansible-vault encrypt_string 'string_to_encrypt' --ask-vault-pass  --name 'encrypt_var_name'
```
- [ ] create a vault to store all var you want to hide ( for group cluster )
```
$ ansible-vault create group_vars/cluster/vault
```
- [ ] edit a vault to store all var you want to hide ( for group cluster )
```
$ ansible-vault edit group_vars/cluster/vault
```

## And you are now able to connect to those hosts, try the command below to test the connection

```
$ ansible -m ping -i inventory all #test the connection
```

## Run a playbook

- [ ] this cmd will ask for vault password use to encrypt encrypt_var used in the playbook
```
$ ansible-playbook -i inventory main.yml --ask-vault-password

***