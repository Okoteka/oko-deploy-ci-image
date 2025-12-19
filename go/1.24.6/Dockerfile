FROM golang:1.24.6-alpine

COPY internal.crt /usr/local/share/ca-certificates/

RUN update-ca-certificates

CMD ["go", "version"]
