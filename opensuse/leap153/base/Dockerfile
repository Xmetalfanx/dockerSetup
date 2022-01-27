FROM opensuse/leap:15.3
#FROM opensuse/tumbleweed

LABEL maintainer="Xmetalfanx@yahoo.com"

#RUN zypper install sudo

# RUN useradd -ms /bin/bash xmetal

# USER xmetal
# WORKDIR /home/xmetal

# Upgrade 
# up for leap 
# dup for tumbleweed 
RUN zypper up
#RUN zypper dup 

# Some software needed for my scripts
RUN zypper install curl wget lsb lsb-release nano git inxi

# get scripts
# RUN git clone -b development https://github.com/Xmetalfanx/linuxSetup.git /home/linuxSetup
