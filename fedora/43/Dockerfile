FROM fedora:43
LABEL maintainer="Xmetalfanx@yahoo.com"

# Determine fastest Mirror for dnf
RUN echo "fastestmirror=true" >> /etc/dnf/dnf.conf

# Upgrade 
RUN dnf upgrade -y

# Some software needed for my scripts
# cleanup afterwards
RUN dnf install curl wget redhat-lsb git inxi -y && dnf clean all

# install zsh
RUN dnf install zsh -y && dnf clean all

# install zap package manager
RUN zsh <(curl -s https://raw.githubusercontent.com/zap-zsh/zap/master/install.zsh) --branch release-v1

# start zsh
RUN zsh

# get scripts
# RUN git clone -b development https://github.com/Xmetalfanx/linuxSetup.git /home/linuxSetup
