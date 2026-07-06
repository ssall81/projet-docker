FROM ubuntu:latest
ARG uid
ARG gid
ARG login

# RUN echo "===========Test============"
# RUN echo $uid
# RUN echo $gid
# RUN echo $login

# RUN echo "===========Fin Test============"

RUN apt-get -y update && \
apt-get -y install python3 && \
apt-get -y install python3-numpy && \
apt-get -y install nano && \
groupadd -g $gid developpeur && \
useradd -u $uid -g $gid -m $login
USER $login:developpeur
WORKDIR /home/$login
ENV PYTHONPATH="/home/$login/modules:${PYTHONPATH}"
ENTRYPOINT ["/bin/bash"]