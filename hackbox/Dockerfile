FROM kasmweb/core-ubuntu-bionic:1.10.0
USER root

ENV HOME /home/kasm-default-profile
ENV STARTUPDIR /dockerstartup
ENV INST_SCRIPTS $STARTUPDIR/install
WORKDIR $HOME



RUN apt update -y 
RUN apt upgrade -y 
RUN apt install openvpn -y 
COPY assets/img.png /usr/share/extra/backgrounds/bg_default.png




RUN chown 1000:0 $HOME
RUN $STARTUPDIR/set_user_permission.sh $HOME

ENV HOME /home/kasm-user
WORKDIR #HOME
RUN mkdir -p $HOME && chown -R 1000:0 $HOME
