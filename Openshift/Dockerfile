FROM fedora:latest

RUN dnf -y --setopt=tsflags=nodocs update && \
    dnf -y --setopt=tsflags=nodocs groupinstall 'Minimal Install' && \
    dnf -y --setopt=tsflags=nodocs install certbot && \
    yum clean all
    
RUN /bin/bash -c 'source $HOME/.bashrc; \
echo $HOME'

CMD tail -f /dev/null
