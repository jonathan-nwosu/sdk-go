FROM golang:1.8-alpine
ADD . /go/src/fakebox
RUN go install fakebox

FROM alpine:latest
COPY --from=0 /go/bin/fakebox .
ENV PORT 8080
CMD ["./fakebox"]
