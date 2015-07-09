FROM registry:2.0.1

ADD config.yml /go/src/github.com/docker/distribution/cmd/registry/config.yml
RUN chown -R www-data:www-data /go

USER www-data
