---
title: golangProtoGen问题
date: 2017-11-03 12:50:42
tags: golang
---
这个问题的原因是：
在生成代码之前要先安装go get -u github.com/golang/protobuf/{proto,protoc-gen-go} 并且把GOPATH/bin目录下的protoc-gen-go放到环境变量PATH里面去，否则会报 
protoc-gen-go: program not found or is not executable 
这个错误。 命令如下：
	
	$ go get -u github.com/golang/protobuf/{proto,protoc-gen-go}