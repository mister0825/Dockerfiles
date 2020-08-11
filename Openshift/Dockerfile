FROM fedora:latest

RUN dnf -y --setopt=tsflags=nodocs update && \
    dnf -y --setopt=tsflags=nodocs install certbot && \
    dnf -y --setopt=tsflags=nodocs install httpd && \
    dnf -y --setopt=tsflags=nodocs groupinstall 'Minimal Install' && \
    yum clean all
    
RUN /bin/bash -c 'source $HOME/.bashrc; \
echo $HOME'

CMD /usr/sbin/httpd -D FOREGROUND

EXPOSE 8080
