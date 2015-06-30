FROM ibmcom/db2express-c

# install additional BigFix prerequistes
RUN yum -y install  libpng12.x86_64

#download the installer and expand
RUN curl http://software.bigfix.com/download/bes/92/ServerInstaller_9.2.3.68-rhe6.x86_64.tgz > /ServerInstaller.tgz
RUN tar -xzvf /ServerInstaller.tgz

COPY ./db2-start.sh /
COPY ./bes-install.rsp /
COPY ./bes-install.sh /
COPY ./bes-start.sh /
RUN chmod u+x /db2-start.sh /bes-install.sh /bes-start.sh