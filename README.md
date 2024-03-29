# SetupNewVPSWithAnsible
This Ansible playbook creates a new Linux user and applies minimal security configurations to one or more VPS's.

### How to install
```
git clone https://github.com/ricardotenv/SetupNewVPSWithAnsible.git
cd SetupNewVPSWithAnsible
```

### Add the virtual machine address to the inventory.
```
echo <ip-address> >> hosts
```

### How to run
```
ansible-playbook -i hosts -u root -e "username=$(whoami)" playbook.yml
```

## TO-DO
- [ ] Automatically recognize key type
- [ ] Add SWAP memory with parameters for option and storage space quantity.