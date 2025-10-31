FROM golang:latest AS builder
RUN apt-get install git
WORKDIR /go/src
COPY ./auth-service ./auth-service
COPY ./commons ./commons
RUN go build -C ./auth-service
RUN chmod +x ./auth-service/auth-service
CMD ["./auth-service/auth-service"]
