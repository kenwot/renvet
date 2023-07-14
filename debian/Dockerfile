# docker build -t renvet:deb .

FROM debian:bookworm

LABEL maintainer="Kenown <kenown@msn.com>" \
    name="Venvet" \
    version="deb" \
    description="A Debian 12 (bookworm) base image for Renvet"

RUN apt-get update \
    && apt-get install -y procps vim openssh-server openssh-client iproute2 iputils-ping wget curl lrzsz zip unzip \
    && touch /etc/vim/vimrc.local \
    && echo "source /usr/share/vim/vim90/defaults.vim" >> /etc/vim/vimrc.local \
    && echo "let skip_defaults_vim = 1" >> /etc/vim/vimrc.local \
    && echo "if has('mouse')" >> /etc/vim/vimrc.local \
    && echo "  set mouse=r" >> /etc/vim/vimrc.local \
    && echo "endif" >> /etc/vim/vimrc.local \
    && echo "alias ls='ls --color=auto'" >> ~/.bashrc \
    && echo "alias ll='ls --color=auto -l'" >> ~/.bashrc \
    && echo "alias la='ls --color=auto -lA'" >> ~/.bashrc \
    && /bin/bash -c 'source ~/.bashrc' \
    && echo "PermitRootLogin yes" >> /etc/ssh/sshd_config \
    && echo "PasswordAuthentication yes" >> /etc/ssh/sshd_config \
    && echo "UseDNS no" >> /etc/ssh/sshd_config \
    && mkdir /run/sshd && echo "root:root" | chpasswd

VOLUME /hostel

EXPOSE 22

CMD ["/usr/sbin/sshd", "-D"]
