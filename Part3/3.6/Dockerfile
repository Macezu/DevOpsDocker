#Build
FROM golang:1.13-alpine3.11 AS build
RUN mkdir /build
ADD *.go /build/
WORKDIR /build

RUN CGO_ENABLED=0 GOOS=linux go build -a -o golang-memtest .

#Production
FROM scratch

COPY --from=builder /build/golang-memtest .

EXPOSE 8080

ENV REQUEST_ORIGIN=http://localhost:5000

CMD ["./server"] 
