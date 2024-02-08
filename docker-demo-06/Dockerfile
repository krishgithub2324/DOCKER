FROM ubuntu:latest
LABEL key="krish"
RUN apt-get update
RUN apt-get install wget openssh-server -y
RUN sed -i 's/PermitRootLogin prohibit-password/PermitRootLogin yes/' /etc/ssh/ssh_config
RUN echo 'root:krish2324' | chpasswd
RUN mkdir /var/run/sshd
CMD ["/usr/sbin/sshd", "-D"]
EXPOSE 22
