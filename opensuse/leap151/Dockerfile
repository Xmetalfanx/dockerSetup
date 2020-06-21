
FROM opensuse/leap:15.1
#FROM opensuse/tumbleweed

MAINTAINER xmetal Xmetalfanx@yahoo.com

# Upgrade 
# up for leap 
# dup for tumbleweed 
RUN zypper up
#RUN zypper dup 

# Some software needed for my scripts
RUN zypper --non-interactive install curl wget lsb-release nano git inxi

# get scripts 
# RUN git clone -b arrayTestingEOL https://github.com/Xmetalfanx/linuxSetup.git /home/
