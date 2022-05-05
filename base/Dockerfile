FROM lucifer8591/rabbit_erlangbase:latest
LABEL MAINTAINER="Kailash K Yogeshwar <kailashyogeshwar85@gmail.com>"
LABEL REPO="lucifer8591/rabbitmq_base:3.8.27"
LABEL build_date="03-09-2019"

WORKDIR /rabbitmq/
RUN wget https://github.com/rabbitmq/rabbitmq-server/releases/download/v3.8.27/rabbitmq-server-generic-unix-3.8.27.tar.xz

RUN tar -xvf rabbitmq-server-generic-unix-3.8.27.tar.xz

RUN echo "Updating PATH env"

RUN echo "export PATH=$PATH:/rabbitmq/rabbitmq_server-3.8.27/sbin" >> ~/.bashrc && . ~/.bashrc

ADD plugins.sh .
RUN chmod +x plugins.sh && ls -l
RUN "/rabbitmq/plugins.sh"
