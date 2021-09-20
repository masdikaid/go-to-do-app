FROM golang:alpine3.14
COPY . /code
WORKDIR /code
RUN go mod vendor
RUN go build -o app main.go
EXPOSE 8080
CMD ./app