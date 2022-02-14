# ansible_kubernetes_cluster_exemple
Try to automate Kubernetes cluster configuration using Ansible 🛠️⚙️💡

$ ssh-keygen #on all host where you want to connect via ssh \n
$ ssh-copy-id username@ip-addr #ip-addr of host where you generate ssh key\n
And you are now able to connect to those hosts, try the command below to test the connection\n
$ ansible -m ping -i inventory all #test the connection\n

Run a playbook : \n
$ansible-playbook -i inventory main.yml\n
