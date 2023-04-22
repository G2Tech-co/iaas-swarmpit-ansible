# G2 Ansible IaC (Infrastructure as code) Setup swarmpit monitoring system for docker swarm control plane (master)

[Ansible doc](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)

## Roles
- [x] swarmpit

## Setup
```sh
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

## Run
Add ssh config host name to `hosts`
```sh
ansible-playbook setup.yml --syntax-check
ansible-playbook setup.yml
```

## Test
```sh
docker stack ps swarmpit
docker service logs swarmpit_app
```
