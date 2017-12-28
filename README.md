# docker-presto
Facebook Presto docker image for development and testing purposes. Forked from [docker-presto] (https://github.com/zhicwu/docker-presto.git)

## What's inside
```
ubuntu:14.04
 |
 |--- zhicwu/java:8
       |
       |--- presto:latest
```
* Official Ubuntu Trusty(14.04) docker image
* Oracle JDK 8u144
* [Facebook Presto](http://prestodb.io/) latest release (0.191)

## How to use
- Setup scripts
```
# git clone https://github.com/prakashdivyy/docker-presto.git
# cd docker-presto
# chmod +x *.sh
```
- Build the image
```
# docker build -t presto .
```
- Start Presto
```
# ./start-presto.sh
# docker logs -f my-presto
...
# docker exec -it my-presto bash
# cd /presto
# ./presto --server presto:8080 --catalog jmx --schema jmx
presto:jmx> show tables;
```