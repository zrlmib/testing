ARG ARCH
FROM multiarch/ubuntu-core:${ARCH}-bionic

RUN apt-get update -qq
RUN apt-get upgrade -y
RUN apt-get dist-upgrade -y
RUN apt-get install -y gcc
RUN apt-get install -y autoconf automake git libssl-dev libtool make unzip wget zlib1g-dev
RUN apt-get install -y doxygen graphviz xsltproc 
RUN apt-get install -y python3 python3-nose python3-rednose python3-pytest
RUN apt-get install -y python3-pip
RUN apt-get install -y docker.io
RUN pip3 install pytest-xdist

ADD entrypoint.sh /root/entrypoint.sh
ENTRYPOINT ["/root/entrypoint.sh"]

LABEL com.circleci.preserve-entrypoint=true

#ENTRYPOINT bash
CMD ["/bin/bash"]
