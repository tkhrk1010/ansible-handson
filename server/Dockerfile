#TODO: もっと軽くする
FROM amazonlinux:latest

RUN yum -y install openssh-server

# when sshd, pubkey is needed
RUN ssh-keygen -f /etc/ssh/ssh_host_rsa_key -N '' -t rsa
RUN ssh-keygen -f /etc/ssh/ssh_host_ecdsa_key -N '' -t ecdsa

# root login
RUN sed -ri 's/^#PermitEmptyPasswords no/PermitEmptyPasswords yes/' /etc/ssh/sshd_config

# root password
RUN echo "root:" | chpasswd

EXPOSE 22

# start sshd
CMD ["/usr/sbin/sshd", "-D"]
