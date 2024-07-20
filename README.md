# Ansible at scale - working with multiple  environments
## Demo repository

To reproduce:
- Create three Ubuntu Server 24.04 machines or later.
- On your developer PC (where you will be running `ansible-playbook` from), create hosts entries in `/etc/hosts` for the machines pointing the hostnames from the `hosts` file to the relevant IPs.
- Configure SSH key authentication on the machines or be lazy like me and enable root password login by modifying `/etc/ssh/sshd_config`, setting `PermitRootLogin yes`.
- Set the password of the `root` users in each machine to the same password (note: NOT recommended for production! This is where using keys becomes convenient and safer).
- On your developer PC run `ansible-playbook -i environments/ubuntu playbooks/ubuntu.yml --ask-pass` and type in the root password you just configured (leave out `--ass-pass` if you are using keys).

Congratulations, you now have three apache servers!

Please refer to the Medium article for further details.

