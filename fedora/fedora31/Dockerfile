FROM fedora:31
MAINTAINER xmetal Xmetalfanx@yahoo.com

# Determine fastest Mirror for dnf
RUN su -c 'echo "fastestmirror=true" >> /etc/dnf/dnf.conf'

# Upgrade 
RUN dnf upgrade -y

# Some software needed for my scripts
RUN dnf install curl wget redhat-lsb-core nano git inxi -y

# get scripts 
RUN git clone -b arrayTestingEOL https://github.com/Xmetalfanx/linuxSetup.git /home/
