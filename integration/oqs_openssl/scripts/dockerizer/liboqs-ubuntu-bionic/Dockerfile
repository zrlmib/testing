From ubuntu:18.04

ENV DEBIAN_FRONTEND noninteractive

RUN apt update -y
RUN apt upgrade -y

RUN useradd -ms /bin/bash oqssa

ADD oqssa /opt/oqssa
RUN echo 'export PATH=/opt/oqssa/bin:$PATH' >> /home/oqssa/.bashrc

# Default command to run
USER oqssa
WORKDIR /home/oqssa
ENTRYPOINT ["/opt/oqssa/bin/oqs-entrypoint.sh"]
CMD ["/bin/bash"]
