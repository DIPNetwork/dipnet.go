<<<<<<< HEAD
<<<<<<< HEAD
<<<<<<< HEAD
#源镜像
=======
>>>>>>> 0a76a03... fix dockerfile
FROM golang:latest
=======
FROM docker.io/golang
>>>>>>> 6198af5... fix dockerfile

ENV GOROOT /usr/local/go
ENV GOBIN $GOROOT/bin
ENV GOPATH /usr/local/go/go_workpace
ENV PATH $PATH:$GOPATH:$GOBIN:$GOROOT

RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install vim-gtk -y
RUN mkdir /usr/local/go/go_workpace
RUN mkdir /usr/local/go/go_workpace/src
RUN mkdir /usr/local/go/go_workpace/pkg
RUN mkdir /usr/local/go/go_workpace/bin

WORKDIR /usr/local/go/go_workpace/src/dpinet_dpos/go-ethereum
ADD . /usr/local/go/go_workpace/src/dpinet_dpos/go-ethereum

RUN go run build/ci.go install ./cmd/geth
EXPOSE 8545 8546 30303 30303/udp 30304/udp

#RUN sed -i '$a export GOROOT=/usr/local/go' /etc/profile
#RUN sed -i '$a export GOBIN=$GOROOT/bin'  /etc/profile
#RUN sed -i '$a export GOPATH=/usr/local/go/go_workpace'  /etc/profile
#RUN sed -i '$a export PATH=$PATH:$GOPATH:$GOBIN:$GOROOT'  /etc/profile
#go构建可执行文件
#RUN go build ./cmd/geth/
#最终运行docker的命令
<<<<<<< HEAD
ENTRYPOINT  ["./geth"]
=======
# Build Gdpn

FROM docker.io/golang

#RUN apt-get update
#RUN apt-get upgrade -y
#RUN apt-get install vim-gtk
WORKDIR /dpinet_dpos/go-ethereum
ADD . /dpinet_dpos/go-ethereum
EXPOSE 8545 8546 30303 30303/udp 30304/udp
>>>>>>> a5332f9... add Dockerfile
=======
#ENTRYPOINT  ["./geth"]
>>>>>>> c719ffb... fix dockerfile
