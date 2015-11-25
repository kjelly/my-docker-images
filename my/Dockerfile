FROM ubuntu:14.04

RUN apt-get update && apt-get install -y git python-dev libyaml-dev python-pip unzip && pip install ansible && git clone https://github.com/ya790206/auto_config /root/auto_config

ADD site.yml /root/auto_config/site.yml

RUN ansible-playbook -i /root/auto_config/hosts /root/auto_config/site.yml  --extra-vars "ansible_user=root" -vvvv

CMD "/bin/bash"
