FROM golang:1.20 as builder

WORKDIR /root

COPY target/go.mod target/go.sum .
RUN go mod download

ENTRYPOINT ["tail", "-f", "/dev/null"]