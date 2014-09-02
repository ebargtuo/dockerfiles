FROM ubuntu:14.04

RUN useradd -m -s /bin/bash -G sudo docker

RUN sed -i 's/%sudo\tALL=(ALL:ALL) ALL/%sudo\tALL=(ALL:ALL) NOPASSWD:ALL/' /etc/sudoers

USER docker

WORKDIR /home/docker

CMD /bin/bash
