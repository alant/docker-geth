FROM ubuntu:xenial

RUN apt-get update \ 
    && apt-get install -y software-properties-common \
    && add-apt-repository -y ppa:ethereum/ethereum \
    && apt-get update \
    && apt-get install -y ethereum \
    && mkdir -p /home/ubuntu/sunnynet_node_test

WORKDIR "/home/ubuntu/sunnynet_node_test"

ENV nodekeyhex="84ba012c18d64c6b128e0d4052f2e444ca9cf7068f4938adc4fdaadb367449fade42a7546247faa45069bdef7428d4c46e2ee7d71840e15e7d478aeaa21395c4"
CMD exec ./bootnode -nodekeyhex $nodekeyhex -verbosity 9 -addr :30318

EXPOSE 30318/udp
