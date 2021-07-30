FROM golang:latest
RUN mkdir -p /go/src/app
WORKDIR /go/src/app
RUN apt-get -y update && apt-get -y install git
COPY . .
RUN go mod download
EXPOSE 60000
ENTRYPOINT go run main.go
