# BPMN gRPC

## Install RPC module

```
go get -u google.golang.org/grpc
go get -u github.com/golang/protobuf/protoc-gen-go
```

```
sudo apt install protobuf-compiler
```

Adding the following lines to .bashrc (for Ubuntu):
```
export GOROOT=/usr/lib/go
export GOPATH=$HOME/go
export GOBIN=$GOPATH/bin
export PATH=$PATH:$GOROOT:$GOPATH:$GOBIN
```

## Build for Golang
build:
```
protoc --go_out=plugins=grpc:$(go env GOPATH)/src/bpmn.proto bpmn.proto
```
use:
```
pb "bpmn.proto"
```
