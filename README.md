création du compte ansible
--------------------------

créer un compte ansible avec les droits sudo

Installation SSH key
--------------------

<p>ssh-keygen -t rsa</p>
<p>ssh-copy-id -i ~/.ssh/id_rsa.pub ansible@VM1 && ssh-copy-id -i ~/.ssh/id_rsa.pub ansible@VM2 && ssh-copy-id -i ~/.ssh/id_rsa.pub ansible@VM3</p> 

ou avec les adresses ip

<p>ssh-copy-id -i ~/.ssh/id_rsa.pub ansible@193.168.1.155 && ssh-copy-id -i ~/.ssh/id_rsa.pub ansible@193.168.1.156 && ssh-copy-id -i ~/.ssh/id_rsa.pub ansible@193.168.1.157</p>

commande ansible
-----------------

<p>all     : ansible-playbook -i inventory/dev/hosts playbook.yml -user=ansible --ask-become-pass --become</p>
<p>partial : ansible-playbook -i inventory/dev/hosts playbook.yml --start-at-task="install packages" -user=ansible --ask-become-pass --become</p>
<p>etape   : ansible-playbook -i inventory/dev/hosts playbook.yml -user=ansible --ask-become-pass --become --step</p>
