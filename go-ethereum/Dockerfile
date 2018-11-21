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
