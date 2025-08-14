# OpenSUSE Tumbleweed Docker Images
## Goal

These images are for testing my linuxSetup scripts when I wouldn't need a full VM to test basic commands 

## Images
### Base Images
These are basically the ubuntu Image that is named + updating/upgrading + adding a few tools (that my scripts DO check for and install on bare metal or vm installs but sometimes there are issues with docker and my checks so i just preinstall these tools)

## Code (template) for my Dockerfile

```
FROM opensuse/tumbleweed
LABEL maintainer="Xmetalfanx@yahoo.com"

# Upgrade
RUN zypper dup

# Some software needed for my scripts
RUN zypper --non-interactive install curl wget lsb-release git inxi

# get scripts
# COMMENTED OUT for now but this would get my scripts and put you in the script's directory
#RUN git clone -b development https://github.com/Xmetalfanx/linuxSetup.git /home/
#WORKDIR /home/linuxSetup/

```

## Naming Conventions for repos 

- examples
  - xmetal/distrobase:description
  - xmetal/ubuntu:focal_base

## Thoughs/Brainstorm 
- an "issue" i see is that the images install some things needed for my scripts to work but my scripts SHOULD install those things anyway 
  - should I comment the lines to install those things in the Dockerfile out?  or since i know they work everytime I have tested something else out, to leave that "as-is" since it may not matter ... if i did comment those lines out in my Dockerfiles, as soon as I git clone and run my scripts the same exact things would be installed anyway
  - the POINT is that I know my script's code to install those things does work 

