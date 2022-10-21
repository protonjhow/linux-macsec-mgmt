# linux-macsec-mgmt
little ansible PoC to manage macsec on linux

Make a new inventory and add a group_vars with appropriate content

```
cp jhowtest myinventory
# update myinventory to reflect your hostnames and IPs of your devices

cp group_vars/jhowtest group_vars/myinventory
# update myinventory to reflect your username/ssh key file, and the physical interface you plan to use in that lab. it should NOT be the interface used to administer the VM!

cp host_vars/macsec1.yaml host_vars/myhost1.yaml
cp host_vars/macsec2.yaml host_vars/myhost2.yaml 
# update the neighbour: reference to the hostname in your inventory
```

Deploy with your own inventory like so: `ansible-playbook -i myinventory site.yaml`

Check feedback from the system with `ansible -i myinventory all -m command -a 'ip macsec show' `
