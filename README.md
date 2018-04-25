# Vagrant + Ansible Example

## Why Vagrant

It helps to quickly provision local VMs for experiments like this one. 

Vagrant is **not** needed with Ansible. It's just here to support the example.

## Why Ansible

It provides a declarative and repeatable format for provisioning VM infrastructure. 

## Steps 

 - Install virtualbox, or the another VM tool supported by Vagrant
 - Install ansible (mac: brew install ansible, Windows?...)
 - Install Vagrant
 - Use minimal/xenial64 as the "box"
 - The vagrant file I used is in the Git repo
    
        git clone https://github.com/mfriedman-upchain/ansible-exp.git
        cd ansible-exp
        vagrant up
 
This should result in 2 vms running locally. 

You can do then do the following (or use your browser):

    curl localhost:9990 
 
You'll see the nginx welcome page. 

## Key Ansible Concepts

 - Playbooks
 - Inventory (look it up you won't really see it in this example)
 - There's a lot more to Ansible. 
 
## References 
 
 - http://docs.ansible.com/ansible/latest/scenario_guides/guide_vagrant.html
 - https://adamcod.es/2014/09/23/vagrant-ansible-quickstart-tutorial.html
 
