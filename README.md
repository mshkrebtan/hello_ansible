Tested on Debian Stretch with Docker 1.12.6-cs13.

## Run the playbook

~~~
ansible-playbook -i hosts.yml -e @extra_vars.yml playbook_main.yml
~~~

## Connect to container one

~~~
ssh docker_root@127.0.0.1 -p 2222
~~~
