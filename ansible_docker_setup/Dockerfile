FROM ubuntu:20.04

RUN apt-get update && \
    DEBIAN_FRONTEND=noninteractive apt-get install -y \
        openssh-client \
        python3 \
        python3-pip \
        sshpass && \
    rm -rf /var/lib/apt/lists/*

RUN python3 -m pip install --upgrade "pip<24.1" && \
    python3 -m pip install "ansible==2.9.12" && \
    pip install boto3

RUN ansible --version
