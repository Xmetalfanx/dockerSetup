FROM archlinux
LABEL maintainer="Xmetalfanx@yahoo.com"

RUN pacman -Syy

# Install package needed to optimize repos
RUN pacman --noconfirm -S pacman-contrib

# Backup mirrorlist
RUN cp /etc/pacman.d/mirrorlist /etc/pacman.d/mirrorlist.backup

# Optmize repos
RUN rankmirrors -v -n 6 /etc/pacman.d/mirrorlist.backup | tee /etc/pacman.d/mirrorlist

# Update the system 
RUN pacman --noconfirm -Syyu

# Some software needed for my scripts
RUN pacman --noconfirm -S curl wget lsb-release  git 

# inxi is in the AUR

# get scripts
# RUN git clone -b development https://github.com/Xmetalfanx/linuxSetup.git /home/linuxSetup
