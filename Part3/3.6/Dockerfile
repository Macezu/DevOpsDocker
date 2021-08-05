#Build
FROM golang:1.17rc1 AS build

WORKDIR /usr/src/

RUN go get -d -v golang.org/x/net/html 

COPY app.go ./home

RUN CGO_ENABLED=0 GOOS=linux go build -a -installsuffix cgo -o app .

#Production
FROM scratch

WORKDIR /home

COPY --from=build /usr/src/app ./
EXPOSE 8080

ENV REQUEST_ORIGIN=http://localhost:5000

CMD ["./server"] 
