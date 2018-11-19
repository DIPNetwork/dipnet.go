<<<<<<< HEAD
#源镜像
FROM golang:latest
#作者
MAINTAINER Razil "zhongmou"
#设置工作目录
WORKDIR $GOPATH/src/dpinet_dpos
#将服务器的go工程代码加入到docker容器中
ADD . $GOPATH/src/dpinet_dpos
#go构建可执行文件
RUN cd /go-ethereum/cmd/geth && go build .
#暴露端口
EXPOSE 8545 8546 30303 30303/udp 30304/udp
#最终运行docker的命令
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
