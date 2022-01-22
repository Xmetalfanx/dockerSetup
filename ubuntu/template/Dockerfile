FROM ubuntu
LABEL maintainer="Xmetalfanx@yahoo.com"

# Update the system
RUN apt-get -y update
RUN apt-get -y upgrade

# set your timezone
RUN ln -fs /usr/share/zoneinfo/America/New_York /etc/localtime
RUN apt-get install -y tzdata
RUN dpkg-reconfigure --frontend noninteractive tzdata


# nano for editing ... not needed by scripts
# my scripts on real systems and vms will check for these and install if needed ... i feel this is just easier preinstalling them in Docker 
RUN apt-get install -y curl wget lsb nano git inxi 

# get scripts 
RUN git clone -b development https://github.com/Xmetalfanx/linuxSetup.git /home/
RUN cd linuxSetup