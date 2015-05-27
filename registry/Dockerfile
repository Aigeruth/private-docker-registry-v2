FROM registry:2.0.1

RUN groupadd -g 31337 deploy &&\
    useradd -u 31337 -g deploy -s /bin/false -M deploy

ADD config.yml /go/src/github.com/docker/distribution/cmd/registry/config.yml
RUN chown -R deploy:deploy /go

USER deploy
