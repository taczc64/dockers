FROM ubuntu:16.04
LABEL maintaine="tangzc64@163.com"
RUN mkdir /root/package
COPY ./go1.9.1.linux-amd64.tar.gz /root/package
ADD ./sources.list /etc/apt/sources.list
WORKDIR /root/package
RUN 	apt-get update	&& \
	apt-get install -y build-essential && \
	tar -zxf go1.9.1.linux-amd64.tar.gz && \
	mv ./go /usr/local && \
	mkdir -p /root/goprojects \
	/root/goprojects/src \
	/root/goprojects/pkg \
	/root/goprojects/bin && \
	apt-get install -y vim && \
	apt-get clean && \
	apt-get autoclean && \
	rm -rf /root/package/go1.9.1.linux-amd64.tar.gz /tmp/* /var/tmp/*
WORKDIR /root
ENV GOROOT=/usr/local/go
ENV GOBIN=$GOROOT/bin
ENV GOPATH=/root/goprojects
ENV PATH=$PATH:$GOBIN:$GOPATH/bin

CMD ["/bin/bash"]
