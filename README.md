# Ansible playbook for ElastAlert
Ansible playbook to install Docker and run Elastalert container - http://github.com/chaitanyaenr/docker-elastalert on Elasticsearch hosts.

## Requirements
You need to have these installed on your host
   - Ansible
   - python

## Add your Elasticsearch hosts
Add your elasticsearch hosts in the hosts file under [Elasticsearch] group.

## Run 

By default, $ ansible-playbook site.yml assumes that the config.yaml file, rules/ are at /tmp/config.yaml /tmp/rules/

Running the below command will install docker, pulls the elastalert image and run the container on the hosts mentioned in inventory file

$ ansible-playbook site.yml

You can override the variables like

$ ansible-playbook --extra-vars '{"FILES_DIR":"/tmp"}' site.yml 


