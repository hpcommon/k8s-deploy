FROM alpine:latest

ARG KUBE_LATEST_VERSION=v1.15.0



# RUN apk add --update ca-certificates

RUN apk add --update -t deps curl

RUN curl -L https://storage.googleapis.com/kubernetes-release/release/${KUBE_LATEST_VERSION}/bin/linux/amd64/kubectl -o /usr/local/bin/kubectl

RUN chmod +x /usr/local/bin/kubectl

RUN apk del --purge deps

RUN rm /var/cache/apk/*
