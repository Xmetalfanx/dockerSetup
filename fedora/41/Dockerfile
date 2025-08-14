FROM fedora:41
LABEL maintainer="Xmetalfanx@yahoo.com"

# Determine fastest Mirror for dnf
RUN echo "fastestmirror=true" >> /etc/dnf/dnf.conf

# Upgrade 
RUN dnf upgrade -y

# Some software needed for my scripts
## redhat-lsb-core may be wrong ... lsb_release maybe the new package 
RUN dnf install curl wget redhat-lsb-core nano git inxi -y

# get scripts 
# RUN git clone -b development https://github.com/Xmetalfanx/linuxSetup.git /home/linuxSetup
