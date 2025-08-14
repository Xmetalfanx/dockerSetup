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


# get scripts
# RUN git clone -b development https://github.com/Xmetalfanx/linuxSetup.git /home/linuxSetup
