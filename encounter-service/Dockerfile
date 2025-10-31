FROM golang:latest AS builder
RUN apt-get install git
WORKDIR /go/src
COPY ./encounter-service ./encounter-service
COPY ./commons ./commons
RUN go build -C ./encounter-service
RUN chmod +x ./encounter-service/encounter-service encounter-service/resources/init.sql
CMD ["./encounter-service/encounter-service"]
