FROM opensuse/tumbleweed 
LABEL maintainer="Xmetalfanx@yahoo.com"

# Upgrade 
# up for leap 
# dup for tumbleweed 
RUN zypper dup 

# Some software needed for my scripts
RUN zypper --non-interactive install curl wget lsb-release nano git inxi

# get scripts
# RUN git clone -b development https://github.com/Xmetalfanx/linuxSetup.git /home/linuxSetup
