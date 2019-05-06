[Test Suite for Linked Data Platform 1.0](http://w3c.github.io/ldp-testsuite)

[![Build Status](https://travis-ci.com/trellis-ldp/ldp-testsuite.svg?branch=master)](https://travis-ci.com/trellis-ldp/ldp-testsuite)

This project is a fork of the W3C LDP testsuite.

```sh
cd dockerfiles/tester/
docker build -t tester .
cd ../dockerfiles/inrupt-pod-server
docker build -t inrupt-pod-server .
cd ../dockerfiles/trellis
docker build -t trellis .
cd ../dockerfiles/node-solid-server
docker build -t node-solid-server .
cd ../dockerfiles/gold
docker build -t gold .
cd ../dockerfiles/rww-play
docker build -t rww-play .
cd ../..
docker network create testnet
docker run -p 8080:8080 -d --name=server --network=testnet inrupt-pod-server
docker run -d  --name=client --network=testnet tester
