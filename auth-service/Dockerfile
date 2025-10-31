FROM golang:alpine
RUN apk add --no-cache git
WORKDIR /go/src
COPY ./auth-service ./auth-service
COPY ./commons ./commons
RUN go build -C ./auth-service
RUN chmod +x ./auth-service/auth-service
CMD ["./auth-service/auth-service"]
