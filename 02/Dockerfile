# syntax=docker/dockerfile:1
FROM golang:1.21.5-alpine
RUN apk add curl
WORKDIR /app
COPY go.mod ./
COPY go.sum ./
RUN go mod download
COPY *.go ./
RUN go build -o /task_manager
EXPOSE 8080
CMD ["/task_manager"]
