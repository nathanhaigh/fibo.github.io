

From CentOS project [site](http://www.centos.org/)

> The CentOS Project is pleased to [announce](http://lists.centos.org/pipermail/centos-announce/2014-July/020393.html) the immediate availability of CentOS 7 for x86_64, including images for [docker](https://registry.hub.docker.com/_/centos/) , and various cloud providers.

installo Centos7 su macchina virtuale

yum docker install
service docker start
chkconfig docker on
docker pull centos
docker images centos

voglio installare Unica, usando un container centos6 e poter fare varie prove
il vantaggio è che posso avere i vari layer separati

oracle
java
weblogic
optimizer
campaign
cognos

procedo quindi

dunque, parto dalla centos6

[root@molo ~]# docker ps
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
[root@molo ~]# docker run centos:centos6 cat /etc/centos-release
CentOS release 6.5 (Final)
[root@molo ~]# docker ps
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES

mmh, come faccio a far partire il container con la centos6 ?
Inoltre voglio partire installando Oracle express


Ok, ho la centos6
come faccio a copiare dei file per installare Oracle? Ho gli rpm da eseguire e anche i file da modificare


come faccio ad aprire una sessione nel mio container ?

[root@molo ~]# docker ps -a
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
[root@molo ~]# docker images
REPOSITORY          TAG                 IMAGE ID            CREATED             VIRTUAL SIZE
scratch             latest              fd230cd6967c        18 hours ago        0 B
centos              centos5             d5844d902074        2 days ago          467.1 MB
centos              centos6             ac1f1b8dce20        2 days ago          212.7 MB
centos              centos7             a5fd0258f31c        2 days ago          224 MB
centos              latest              a5fd0258f31c        2 days ago          224 MB
[root@molo ~]# sudo docker run -t -i centos:centos6 /bin/bash
bash-4.1# exit
exit
[root@molo ~]# docker ps -a
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS                     PORTS               NAMES
f5b5f056b716        centos:centos6      /bin/bash           7 seconds ago       Exited (0) 2 seconds ago                       berserk_lumiere0  

vedi risposta su stackoverflow e aggiungi link a questo articolo
http://stackoverflow.com/questions/17903705/is-it-possible-to-start-a-shell-session-in-a-running-container-without-ssh/26117612#26117612



