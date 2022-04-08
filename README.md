Client adress : 10.0.10.4
Server adress : 10.0.10.3

main commands:

--Check syntax
ansible-lint my_file.yaml

--Trigger a playbook between client and server
ansible-playbook -i hosts deploy.yaml

--Using vault method:
--Encrypt password
ansible-vault encrypt credentials.yml

--Trigger playbook with encrypted password
ansible-playbook -i hosts.yml --ask-vault-pass deploy.yml

--Using ssh key method:
--Generate ssh key from server
ssh-keygen -t rsa

--Copy public key to client
ssh-copy-id admin@10.0.10.4

--Check copied key client side
cat .ssh/authorized_keys
