# OpenSUSE Tumbleweed Docker Images
## Goal

These images are for testing my linuxSetup scripts when I wouldn't need a full VM to test basic commands 

## Images
### Base Images
These are basically the ubuntu Image that is named + updating/upgrading + adding a few tools (that my scripts DO check for and install on bare metal or vm installs but sometimes there are issues with docker and my checks so i just preinstall these tools)

## Code (template) for my Dockerfile

```
FROM opensuse/tumbleweed
MAINTAINER xmetal Xmetalfanx@yahoo.com

# Upgrade
RUN zypper dup

# Some software needed for my scripts
RUN zypper --non-interactive install curl wget lsb-release nano git inxi

# get scripts
# COMMENTED OUT for now but this would get my scripts and put you in the script's directory
#RUN git clone -b development https://github.com/Xmetalfanx/linuxSetup.git /home/
#WORKDIR /home/linuxSetup/

```