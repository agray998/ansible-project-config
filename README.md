# Ansible-project-config
This repo contains ansible roles, along with an inventory and playbook, for configuring the following:
* A dev VM with python, docker and docker-compose installed and a specific repo cloned down
* A jenkins server (assumed to have jenkins already installed) with python, docker, docker-compose and an SSH key pair for the jenkins user
* A docker swarm manager with docker installed, a jenkins user set up with the public SSH key generated on the jenkins server as an authorized key, and an SSH environment that defines an environment variable MYSQL_ROOT_PASSWORD (to be set on the command line and passed through using -e when running the playbook)
* A swarm worker with docker installed, set up to be part of the swarm initialised on the swarm manager