# loadbalancer-demo

This is a loadbalancer example with two springboot applications, sending 10% of requests to service1 and 90% of requests to service2. 

![lb drawio (1)](https://user-images.githubusercontent.com/109630016/211205321-b35ed2b3-a9da-435b-a60d-a355d09fc501.png)

Execute these commands to run the docer containers:

- mvn clean install
- docker-compose build
- docker-compose up -d
- for i in {1..30}; do curl http://localhost:9090; done

The result expected of this last command is 27 requests sended to service2 and 3 to service1, like this example:

OKtest2
OKtest2
OKtest2
OKtest2
OKtest2
OKtest2
OKtest2
OKtest2
OKtest2
OKtest1

OKtest2
OKtest2
OKtest2
OKtest2
OKtest2
OKtest2
OKtest2
OKtest2
OKtest2
OKtest1

OKtest2
OKtest2
OKtest2
OKtest2
OKtest2
OKtest1
OKtest2
OKtest2
OKtest2
OKtest2
