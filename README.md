OpenVPN Server Docker Deploy 
====
Ansible script for setting up OpenVPN docker server on VPS.
Generate clients certificates and ovpn configurations

### How to use
1. Change ansible_deploy/inventory.yml for your vps server
2. Change array for your openvpn clients in host_vars
```
- ovpn_clients:
      - name: iphone_ss6
      - name: iphone_ss7
      - name: router
```
3. ```bash deploy.sh``` or ```ansible-playbook -vvvv -i ansible_deploy/inventory.yml ansible_deploy/deploy.yml --ask-sudo-pass``` and promt VPS sudo password
4. Getting result configurations for your clients in directory ```result```


### Security issues
1. Client keys has no password
2. PKI generates without password for starting without promts
