FROM jrei/systemd-ubuntu:18.04
RUN apt-get update
RUN apt-get install -y python3-pip python3 openssh-server
RUN pip3 install --upgrade pip
RUN pip3 install ansible
RUN mkdir -p /root/.ssh
RUN echo "-----BEGIN RSA PRIVATE KEY-----\n\
MIIEpAIBAAKCAQEAveqDAATUrl7c3AG5/WGrL0Mb6lNs7VpYlOflJA32rZP3o0uf\n\
kInB8gphak7XlJBDEId/Au3sqTQq9CVFX/wMTiktA8Rz753nr5br62ZxC871puG8\n\
sLHXG0bK96RqDK7hNdWkG4h/gvnPfBXsSoNLtFawwntTalKi2gZbZhssFJLOatfU\n\
bA3SvqQNNk66cTcEH5R2ugH/IP777MQh2w0djUD513/ilUvYQDzWyxtL6uavMw5g\n\
2WEXscTvK+0ogKCfCWr559AniQrtdnl7kleC65/8Th7irjo66HjBNytSYNzMvhfN\n\
G1Ym8mnpdicwCXkQSLBYiyAAQ3vHjEFeZ5QLewIDAQABAoIBADGjHpQdrxzYDG+w\n\
P9Va9qwGpUAsh9bNe0OIDJrMz4F0oA/dDxpu9vL1BZsMekoJHo4ua+LvHqDm0qc3\n\
Kpe4v9qZ5nsKmKazJb/9+TFwd/F3KTtx2qhwAuHNMfVh0pn4B0LT0O2lUnaAJluv\n\
OzAKevnqgo6CPz4V1RyY9sCML4w8ktZaNEXbx8m0jqjaR8Ew8KzMAeQ94c2Jp/zQ\n\
0a4+PjFhLW5ku5P86myu+t2k++CbNCm7n5YZQH4NkL2LP2hnRD7TK4+t7IrnIpw/\n\
2B7i7oJLD1IghvbVvosXq6/8LmRibB9SDwtfP45Kaho4dKqCe5sk3uticaKwg4nL\n\
w0CkBEECgYEA8fswvU66fHKJfOzGgrnDwgL/+FaMtolfTOISwKIBfnyWjLRXfC9E\n\
aUF+I7/jogsygKq+bxwg2N6bgACWwlIlMilpZegj7rKaGqATLsvSYfZn66pyJh3R\n\
FJlLC6pezghl+5jqGJhWcxK35A60B7sEn2OSY9pZ8moTJvz+KDEq8aECgYEAyOsl\n\
YnforU1edIcIi3qFt8QQKB6uxyTOZTB+I7TiXZCjRTHU7ibkaQmxoP7QoxRuF1pj\n\
Yi2CJVae8C0tC8CImPKbY/s6CSZBCRGTn7JXyxuqQPSAd4acZE4ouH/X2tsqH93X\n\
Y9Ciyb7vfFhcj8n9zXUft+ssxgyrUz4Lb0xJX5sCgYAvolf83BOfzdg8zEtjjnf3\n\
qCmFVFxMzowBEXvJidqrcJEeT53tJ0zbP3Y6SVrhGj0t0O695pacum137CXBSPRj\n\
hH1n/yObqHLnjN1Z1+upNx1L6figgjwXRvnb6QTSoBqbRYXHo61Y57VlYnOUFf+Z\n\
9Lrrhx8vtivg/+p0NQGUIQKBgQC1gmmFqZoUZh782rjHeOqwd3m5JO70jbXACK0M\n\
CO+vY2l8q2YXuB8FHXLRZSKLEXvbsRazrTU0EisIA2f8g/VjZ1kmW+G0PlDmpnBd\n\
Bzr1DIsknz4nvP4wR8PV2fjhiLlnjHx3ehZ2d/3WseT9KZgWMsdy2gza5rsoOpcN\n\
9zcaHQKBgQDAEDKGL5DBdHD8JeTS8x12xK2mrmutrBvK8Q4Wy7eBt4omXpmqkcHB\n\
onKWDRdoEqGJmv+rUjPHPMEWb39yzjzbzgMFecCkLkAm4Q2VAOGzbBx3wCzLVWVq\n\
z/73jTGhAoMGBGxx+cCaZ8eZYqmboMfGo0Fj0WtqV6FkXszf4jGQRw==\n\
-----END RSA PRIVATE KEY-----"\
> /root/.ssh/id_rsa
RUN echo "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQC96oMABNSuXtzcAbn9YasvQxvqU2ztWliU5+UkDfatk/ejS5+QicHyCmFqTteUkEMQh38C7eypNCr0JUVf/AxOKS0DxHPvneevluvrZnELzvWm4bywsdcbRsr3pGoMruE11aQbiH+C+c98FexKg0u0VrDCe1NqUqLaBltmGywUks5q19RsDdK+pA02TrpxNwQflHa6Af8g/vvsxCHbDR2NQPnXf+KVS9hAPNbLG0vq5q8zDmDZYRexxO8r7SiAoJ8Javnn0CeJCu12eXuSV4Lrn/xOHuKuOjroeME3K1Jg3My+F80bVibyael2JzAJeRBIsFiLIABDe8eMQV5nlAt7" > /root/.ssh/id_rsa.pub
RUN echo "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQC96oMABNSuXtzcAbn9YasvQxvqU2ztWliU5+UkDfatk/ejS5+QicHyCmFqTteUkEMQh38C7eypNCr0JUVf/AxOKS0DxHPvneevluvrZnELzvWm4bywsdcbRsr3pGoMruE11aQbiH+C+c98FexKg0u0VrDCe1NqUqLaBltmGywUks5q19RsDdK+pA02TrpxNwQflHa6Af8g/vvsxCHbDR2NQPnXf+KVS9hAPNbLG0vq5q8zDmDZYRexxO8r7SiAoJ8Javnn0CeJCu12eXuSV4Lrn/xOHuKuOjroeME3K1Jg3My+F80bVibyael2JzAJeRBIsFiLIABDe8eMQV5nlAt7" > /root/.ssh/authorized_keys
RUN sed -i 's/PermitRootLogin no/PermitRootLogin yes/g' /etc/ssh/sshd_config
RUN sed -i "s/.*PubkeyAuthentication.*/PubkeyAuthentication yes/g" /etc/ssh/sshd_config
RUN echo "Host *\n\
   StrictHostKeyChecking no\n\
   UserKnownHostsFile=/dev/null"\
> /root/.ssh/config
RUN chmod 0600 -R /root/.ssh
RUN service ssh stop
RUN mkdir -p /var/run/sshd /run/sshd
CMD ["/sbin/init", ";", "/usr/sbin/sshd", "-D"]
