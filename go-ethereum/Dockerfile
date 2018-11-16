#源镜像
FROM golang
#作者
MAINTAINER Razil "zhongmou"
#设置工作目录
WORKDIR $GOPATH/src/dpinet_dpos
#将服务器的go工程代码加入到docker容器中
ADD . $GOPATH/src/dpinet_dpos
#go构建可执行文件
RUN cd /go-ethereum/cmd/ && go build ./geth
#暴露端口
EXPOSE 8545 8546 30303 30303/udp 30304/udp
#最终运行docker的命令
ENTRYPOINT  ["geth"]


# Build Geth in a stock Go builder container
# FROM golang:1.9-alpine as builder

# RUN apk add --no-cache make gcc musl-dev linux-headers

# ADD . /go-ethereum
# RUN cd /go-ethereum && make geth

# Pull Geth into a second stage deploy alpine container
# FROM alpine:latest

# RUN apk add --no-cache ca-certificates
# COPY --from=builder /go-ethereum/build/bin/geth /usr/local/bin/

# EXPOSE 8545 8546 30303 30303/udp 30304/udp
# ENTRYPOINT ["geth"]
