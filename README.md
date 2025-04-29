# SetupNewVPSWithAnsible
This Ansible playbook creates a new Linux user and applies minimal security configurations to one or more VPS's. By default, it disables SSH root login, but this can be changed via a variable.

⚠️ _This playbook was only tested on VPS's running Ubuntu 22 and 24 LTS._

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
# Default run (disables root login)
ansible-playbook -i hosts -u root -e "new_username=$(whoami)" playbook.yml

# To keep root login enabled
ansible-playbook -i hosts -u root -e "new_username=$(whoami)" -e "disable_root_login=false" playbook.yml
```

## TO-DO
- [x] [Add the possibility of disabling root login to be optional](https://github.com/ricardotenv/SetupNewVPSWithAnsible/issues/1)
- [ ] [Enable firewall](https://github.com/ricardotenv/SetupNewVPSWithAnsible/issues/2)
- [ ] [Automatically recognize key type](https://github.com/ricardotenv/SetupNewVPSWithAnsible/issues/3)
- [ ] [Add SWAP memory with parameters for option and storage space quantity](https://github.com/ricardotenv/SetupNewVPSWithAnsible/issues/4)
- [x] Open issues from this list
- [ ] [Convert to CLI application](https://github.com/ricardotenv/SetupNewVPSWithAnsible/issues/5)
- [ ] [Optional Docker installation](https://github.com/ricardotenv/SetupNewVPSWithAnsible/issues/6)
- [ ] [Test on CentOS](https://github.com/ricardotenv/SetupNewVPSWithAnsible/issues/7)
