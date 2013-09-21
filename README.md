ansible-simple-example
======================

Création du template de box

    vagrant add box precise64 http://files.vagrantup.com/precise64.box
    vagrant up

Création des alias ssh (fichier ~/.ssh/config)

    Host dev1
      Hostname 192.168.2.2
      IdentityFile ~/.ssh/id_rsa
      User vagrant

    Host dev2
      Hostname 192.168.2.3
      IdentityFile ~/.ssh/id_rsa
      User vagrant

    Host dev3
      Hostname 192.168.2.4
      IdentityFile ~/.ssh/id_rsa
      User vagrant


Copie des clefs ssh

    cat ~/.ssh/id_rsa.pub | ssh dev1 'cat >> .ssh/authorized_keys'
    cat ~/.ssh/id_rsa.pub | ssh dev2 'cat >> .ssh/authorized_keys'
    cat ~/.ssh/id_rsa.pub | ssh dev3 'cat >> .ssh/authorized_keys'

Création de l'environnement

    ansible-playbook -i production site.yml


