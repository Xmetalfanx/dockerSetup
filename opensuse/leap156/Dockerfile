FROM opensuse/leap:15.6
LABEL maintainer="Xmetalfanx@yahoo.com"

# update the system and install sudo
# This is needed to run the container as a non-root user
# and to allow the user to run commands with sudo without a password
RUN zypper --non-interactive refresh && \
    zypper --non-interactive update && \
    zypper --non-interactive install sudo && \
    groupadd sudo
    
# create a non-root user with sudo privileges    
RUN useradd -m -g users xmetal && \
    echo "xmetal ALL=(ALL) NOPASSWD: ALL" >> /etc/sudoers && \
    usermod -aG sudo xmetal


# Switch to non-root user
USER xmetal
WORKDIR /home/xmetal

# Some software needed for my scripts
# a problem too? 
RUN sudo zypper --non-interactive install curl wget lsb-release git inxi

# get scripts
RUN git clone -b development https://github.com/Xmetalfanx/linuxSetup.git /home/xmetal/Downloads/linuxSetup

RUN cd /home/xmetal/Downloads/linuxSetup
