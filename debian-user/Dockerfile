FROM debian:wheezy

RUN useradd -m -s /bin/bash -G sudo docker

RUN apt-get update && \
    apt-get -y install sudo && \
    apt-get clean && \
    rm -r /var/lib/apt/lists/*

RUN sed -i 's/%sudo\tALL=(ALL:ALL) ALL/%sudo\tALL=(ALL:ALL) NOPASSWD:ALL/' /etc/sudoers

USER docker

WORKDIR /home/docker

CMD /bin/bash
