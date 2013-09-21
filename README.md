ansible-simple-example
======================

Création du template de box

    vagrant add box precise64 http://files.vagrantup.com/precise64.box
    vagrant init

Création de l'environnement

    ansible-playbook -i production site.yml


