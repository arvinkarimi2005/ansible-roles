# migration

Ansible roles for infra configs and deployments
CAUTION: THIS IS NOT GOOD FOR YOUR PRODUCTION, VARIABLES ARE NOT DECLARED CLEARY AND SOME VARIABLES ARE HARDCODED


`ansible-playbook common.yaml -i ./hosts.ini -l jenkins`

#### common.yaml :
1. install ntp
2. install docker, docker-compose
3. set proxy for docker
4. install pip and docker, docker-compose with pip ( for ansible use)
5. docker login to harbor

#### create_ansible_user_and_ops.yaml
- create users and configs on servers
- copy user ssh key
- disables ssh with password login

#### dangerous files:
clear_docker_container_and_images.yaml ( this file is very dangerous, it removes all container and images on vms)

#### dockerize_login_for_ansible_user.yaml
logins in harbor with ansible users for deployments


#### cadvisor_nodeexporter.yaml
install cadvisor and node exporter on dockerize vps for promtheus/

#### install dbs and  create db users
- postgres.yaml (warehouse, notifications)


#### stage.yaml
- install and configs stage infra with one docker-compose file

#### sysctl.yaml
- config os resources such as nofile, swappines, etc

#### dockerize.yaml
1. install redis
2. install mongo
3. install rabbitmq
