FROM ubuntu:20.04

RUN apt-get update && apt-get install git -y
RUN DEBIAN_FRONTEND=noninteractive apt-get install maven -y

RUN git clone https://github.com/miladhub/calculator-servlet-example.git /tmp/calculator-servlet-example
WORKDIR /tmp/calculator-servlet-example
RUN mvn package

RUN mkdir /tmp/trgt && cp /tmp/calculator-servlet-example/target/mycalcwebapp.war /tmp/trgt
