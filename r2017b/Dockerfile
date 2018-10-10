FROM debian:9 as matlab

RUN apt-get update && \
        apt-get install -y wget unzip

WORKDIR /mcr-install

RUN \
        wget -nv http://ssd.mathworks.com/supportfiles/downloads/R2017b/deployment_files/R2017b/installers/glnxa64/MCR_R2017b_glnxa64_installer.zip && \
        unzip MCR_R2017b_glnxa64_installer.zip
RUN \
        mkdir /opt/mcr && \
        ./install -destinationFolder /opt/mcr -agreeToLicense yes -mode silent
RUN \
        rm -rf /mcr-install
