.PHONY: build cluster test

default: build

build:
	go build -o bin/swarm    github.com/happyxie/go-ethereum/cmd/swarm
	go build -o bin/geth     github.com/happyxie/go-ethereum/cmd/geth
	go build -o bin/bootnode github.com/happyxie/go-ethereum/cmd/bootnode

cluster: build
	scripts/boot-cluster.sh

test:
	go test -v github.com/happyxie/go-ethereum/swarm/...
