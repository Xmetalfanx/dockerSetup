FROM opensuse/leap:15.6
LABEL maintainer="Xmetalfanx@yahoo.com"

RUN useradd -ms /bin/bash xmetal

USER xmetal
WORKDIR /home/xmetal

# RUN usermod -aG wheel xmetal

# Upgrade 
RUN zypper --non-interactive ref && \
    zypper --non-interactive up && \
    zypper clean --all

# Some software needed for my scripts
RUN zypper install curl wget lsb lsb-release  git inxi

# get scripts
RUN git clone -b development https://github.com/Xmetalfanx/linuxSetup.git /home/linuxSetup
