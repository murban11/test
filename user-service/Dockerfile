FROM golang:latest AS builder
RUN apt-get install git
WORKDIR /go/src
COPY ./user-service ./user-service
COPY ./commons ./commons
RUN go build -C ./user-service
RUN chmod +x ./user-service/user-service user-service/resources/init.sql
CMD ["./user-service/user-service"]
