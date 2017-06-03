# hass
Server setup

Setting up a remote debian server using ansible

Generate keys:

`ssh-keygen -t rsa -b 4096`

Send keys to server:

`./copy-public-key-prod.sh <sshuser> <vps-server-ip>`

Setup blank server:

`ansible-playbook -v --key-file=ssh/id_rsa bootstrap.yml --user root`

Prepare the server for web stuff:

`ansible-playbook core-setup.yml --user deploy --sudo --ask-sudo-pass`
