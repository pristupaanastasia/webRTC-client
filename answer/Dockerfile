FROM golang:latest
RUN mkdir -p /go/src/app
WORKDIR /go/src/app
RUN apt-get -y update && apt-get -y install git
COPY . .
RUN go mod download
RUN go build -o main .
ENTRYPOINT go run main.go
EXPOSE 6060