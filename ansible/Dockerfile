#TODO: もっと軽くする
FROM ubuntu

WORKDIR /server

ENV ANSIBLE_HOST_KEY_CHECKING False

RUN apt-get update && \
    apt-get install -y software-properties-common && \
    apt-add-repository ppa:ansible/ansible && \
    apt-get update && \
    apt-get install -y ansible

CMD /bin/bash
