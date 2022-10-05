# syntax=docker/dockerfile:1.4
FROM alpine:3.16.2

RUN apk add --no-cache openssh-client git
RUN mkdir -p -m 0700 ~/.ssh && ssh-keyscan github.com >> ~/.ssh/known_hosts
RUN --mount=type=ssh git clone git@github.com:glours/secret-repo.git

CMD ls -lah secret-repo
