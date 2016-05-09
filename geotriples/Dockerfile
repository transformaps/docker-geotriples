FROM ubuntu:14.04
MAINTAINER George Papadakis <gpapadis@di.uoa.gr>

RUN apt-get update && \
    apt-get install -y \
                default-jdk \
                maven \
                git && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

RUN git clone https://github.com/LinkedEOData/GeoTriples.git && \
    cd  GeoTriples/ && \
    mvn package 

RUN echo "alias geotriples-cmd='java -jar /GeoTriples/target/geotriples*cmd.jar'" >> ~/.bashrc
