FROM ubuntu:18.04
RUN apt-get update
RUN apt-get install -y python3 openssh-server
RUN mkdir -p /root/.ssh
RUN echo "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQC96oMABNSuXtzcAbn9YasvQxvqU2ztWliU5+UkDfatk/ejS5+QicHyCmFqTteUkEMQh38C7eypNCr0JUVf/AxOKS0DxHPvneevluvrZnELzvWm4bywsdcbRsr3pGoMruE11aQbiH+C+c98FexKg0u0VrDCe1NqUqLaBltmGywUks5q19RsDdK+pA02TrpxNwQflHa6Af8g/vvsxCHbDR2NQPnXf+KVS9hAPNbLG0vq5q8zDmDZYRexxO8r7SiAoJ8Javnn0CeJCu12eXuSV4Lrn/xOHuKuOjroeME3K1Jg3My+F80bVibyael2JzAJeRBIsFiLIABDe8eMQV5nlAt7" > /root/.ssh/authorized_keys
RUN sed -i 's/PermitRootLogin no/PermitRootLogin yes/g' /etc/ssh/sshd_config
RUN sed -i "s/.*PubkeyAuthentication.*/PubkeyAuthentication yes/g" /etc/ssh/sshd_config
RUN chmod 0600 -R /root/.ssh
RUN service ssh stop
RUN mkdir -p /var/run/sshd /run/sshd
CMD ["/usr/sbin/sshd", "-D"]
