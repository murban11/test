FROM golang:alpine
RUN apk add --no-cache git
WORKDIR /go/src
COPY ./user-service ./user-service
COPY ./commons ./commons
RUN go build -C ./user-service
RUN go clean -modcache
RUN go clean -cache
RUN chmod +x ./user-service/user-service user-service/resources/init.sql
CMD ["./user-service/user-service"]
