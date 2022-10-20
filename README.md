# linux-macsec-mgmt
little ansible PoC to manage macsec on linux

Make a new inventory and add a group_vars with appropriate content

Deploy with your own inventory like so: `ansible-playbook -i jhow-test site.yaml`

Check feedback from the system with `ansible -i jhow-test -m command -a 'ip macsec show'`
