FROM debian:jessie

RUN groupadd -g 31337 deploy &&\
    useradd -u 31337 -g deploy -s /bin/false -M deploy &&\
    mkdir /data &&\
    chown deploy:deploy /data
VOLUME /data
