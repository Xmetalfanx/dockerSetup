FROM ubuntu:bionic
MAINTAINER xmetal Xmetalfanx@yahoo.com

# Update the system
RUN apt-get -y update
RUN apt-get -y upgrade

# set your timezone
RUN ln -fs /usr/share/zoneinfo/America/New_York /etc/localtime
RUN apt-get install -y tzdata
RUN dpkg-reconfigure --frontend noninteractive tzdata

# Install zsh - not really needed 
RUN apt-get install -y zsh
RUN sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# install some dependencies that will not install in docker due to my code using sudo 
# nano for editing ... not needed by scripts
RUN apt-get install -y curl wget lsb nano git inxi 

# get scripts
# RUN git clone -b development https://github.com/Xmetalfanx/linuxSetup.git /home/linuxSetup
