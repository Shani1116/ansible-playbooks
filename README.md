# Sample Playbooks that are useful for day-to-day tasks

## Playbook1.yml -  _A playbook to download and install a file on a server_ 

- Edit the inventory file with correct hostnames and usernames
```sh
/etc/ansible/hosts
[hostname]
server1 ansible_ssh_host=<ip-address> ansible_user=<username>
```
- Provide the private key file in the ansible.cfg file (Else provide the path when executing the playbook)
```sh
/etc/ansible/ansible.cfg
private_key_file = <file path to private key>
```
- Run the playbook
```sh
sudo ansible-playbook -i /etc/ansible/hosts playbook1.yml