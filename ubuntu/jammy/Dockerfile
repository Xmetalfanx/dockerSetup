FROM ubuntu:jammy
LABEL maintainer="Xmetalfanx@yahoo.com"

# Update the system
RUN apt -y update
RUN apt -y upgrade

# set your timezone
RUN ln -fs /usr/share/zoneinfo/America/New_York /etc/localtime
RUN apt install -y tzdata
RUN dpkg-reconfigure --frontend noninteractive tzdata

# install some dependencies that will not install in docker due to my code using sudo 
RUN apt install -y curl wget lsb-release git inxi

# USER xmetal
# WORKDIR /home/xmetal

#RUN usermod -aG wheel xmetal

# Install zsh - not really needed
RUN apt install -y zsh

RUN apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# install zap package manager
# different due to dash being used instead of bash
RUN curl -fsSL https://raw.githubusercontent.com/zap-zsh/zap/master/install.zsh -o /tmp/install.zsh \
    && zsh /tmp/install.zsh --branch release-v1 \
    && rm /tmp/install.zsh

# get scripts
# RUN git clone -b development https://github.com/Xmetalfanx/linuxSetup.git /home/linuxSetup
