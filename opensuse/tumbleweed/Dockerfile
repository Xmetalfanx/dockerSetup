FROM opensuse/tumbleweed 
LABEL maintainer="Xmetalfanx@yahoo.com"

# refresh the repositories and upgrade the system
RUN zypper --non-interactive dup --no-allow-vendor-change

# Some software needed for my scripts
RUN zypper --non-interactive install curl wget lsb-release  git inxi

# Upgrade
# up for leap
# dup for tumbleweed
# code below commented out had issues
# RUN zypper dup
RUN zypper --non-interactive --gpg-auto-import-keys dup

# install zsh
RUN zypper --non-interactive install zsh

# install zap package manager
RUN zsh <(curl -s https://raw.githubusercontent.com/zap-zsh/zap/master/install.zsh) --branch release-v1

# start zsh
RUN zsh


# get scripts
# RUN git clone -b development https://github.com/Xmetalfanx/linuxSetup.git /home/linuxSetup
