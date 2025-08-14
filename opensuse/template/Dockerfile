
FROM opensuse/leap:15.3
#FROM opensuse/tumbleweed

LABEL maintainer="Xmetalfanx@yahoo.com"

# Upgrade 
# up for leap 
# dup for tumbleweed 
RUN zypper up
#RUN zypper dup 



# Some software needed for my scripts
RUN zypper install curl wget redhat-lsb-core  git inxi -y

# get scripts 
RUN git clone -b development https://github.com/Xmetalfanx/linuxSetup.git /home/
