création du compte ansible
--------------------------

créer un compte ansible avec les droits sudo

Installation SSH key
--------------------

ssh-keygen -t rsa
ssh-copy-id -i ~/.ssh/id_rsa.pub ansible@VM1 && ssh-copy-id -i ~/.ssh/id_rsa.pub ansible@VM2 && ssh-copy-id -i ~/.ssh/id_rsa.pub ansible@VM3 

ou avec les addresses ip

ssh-copy-id -i ~/.ssh/id_rsa.pub ansible@193.168.1.155 && ssh-copy-id -i ~/.ssh/id_rsa.pub ansible@193.168.1.156 && ssh-copy-id -i ~/.ssh/id_rsa.pub ansible@193.168.1.157

commande ansible
-----------------

ansible-playbook -i inventory/dev/hosts playbook.yml -user=ansible --ask-become-pass --become