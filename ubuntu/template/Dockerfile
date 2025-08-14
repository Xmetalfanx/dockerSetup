FROM ubuntu
LABEL maintainer="Xmetalfanx@yahoo.com"

# Update the system
RUN apt -y update
RUN apt -y upgrade

# set your timezone
RUN ln -fs /usr/share/zoneinfo/America/New_York /etc/localtime
RUN apt install -y tzdata
RUN dpkg-reconfigure --frontend noninteractive tzdata


#  for editing ... not needed by scripts
# my scripts on real systems and vms will check for these and install if needed ... i feel this is just easier preinstalling them in Docker 
RUN apt install -y curl wget lsb  git inxi 

# get scripts 
RUN git clone -b development https://github.com/Xmetalfanx/linuxSetup.git /home/
RUN cd linuxSetup