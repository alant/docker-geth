FROM ubuntu:xenial

RUN apt-get update \ 
    && apt-get install -y software-properties-common \
    && add-apt-repository -y ppa:ethereum/ethereum \
    && apt-get update \
    && apt-get install -y ethereum \
    && mkdir -p /home/ubuntu/sunnynet_node_test

WORKDIR "/home/ubuntu/sunnynet_node_test"

ENV nodekeyhex="3be27887153ab7e7678219842e405671869c5ff46a9639596148b8f44c4c234a"
CMD exec bootnode -nodekeyhex $nodekeyhex -verbosity 9 -addr :30318

EXPOSE 30318/udp
