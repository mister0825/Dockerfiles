FROM fedora:latest

RUN dnf -y --setopt=tsflags=nodocs update && \
    dnf -y --setopt=tsflags=nodocs install certbot && \
    dnf -y --setopt=tsflags=nodocs install iproute && \
    dnf -y --setopt=tsflags=nodocs groupinstall 'Minimal Install' && \
    dnf clean all
    
RUN /bin/bash -c 'source $HOME/.bashrc; \
echo $HOME'

CMD /usr/bin/tail -f /dev/null

