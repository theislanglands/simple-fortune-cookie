# build stage
FROM golang:1.18
WORKDIR /usr/src/app
COPY *.go ./
#RUN go mod download && go mod verify
COPY . .
RUN go build -v -o /usr/local/bin/frontend ./...
EXPOSE 8080
CMD ["frontend"]

#-e BACKEND_DNS=172.17.0.1 -e BACKEND_PORT=9000