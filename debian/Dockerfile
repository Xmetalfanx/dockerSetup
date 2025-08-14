FROM debian:stable
LABEL maintainer="Xmetalfanx@yahoo.com"

# Update the system
RUN apt -y update
RUN apt -y upgrade

## copied from ubuntu Dockfile ... is this even needed? 
# # set your timezone
# RUN ln -fs /usr/share/zoneinfo/America/New_York /etc/localtime
# RUN apt install -y tzdata
# RUN dpkg-reconfigure --frontend noninteractive tzdata

# install some dependencies that will not install in docker due to my code using sudo 
RUN apt install -y curl wget lsb-base lsb-release git inxi 

# Install zsh - not really needed 
RUN apt install -y zsh
RUN sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# get scripts
# RUN git clone -b development https://github.com/Xmetalfanx/linuxSetup.git /home/linuxSetup
