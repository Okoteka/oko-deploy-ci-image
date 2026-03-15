FROM golang:1.25.7-alpine

COPY internal.crt /usr/local/share/ca-certificates/

RUN update-ca-certificates

RUN apk add --no-cache git openssh

ENV GOPRIVATE=g.nas.loc

RUN mkdir -p /root/.ssh && \
    ssh-keyscan g.nas.loc >> /root/.ssh/known_hosts

RUN git config --global url."ssh://git@g.nas.loc/".insteadOf "https://g.nas.loc/"

RUN wget -O- -nv https://golangci-lint.run/install.sh | sh -s -- -b $(go env GOPATH)/bin v2.11.2

# Install task runner
RUN curl -sSL https://taskfile.dev/install.sh | sh -s -- -b /usr/bin

CMD ["go", "version"]
