FROM golang:1.16-alpine as builder

WORKDIR /go/src/app

COPY main.go /go/src/app

RUN go build main.go


FROM scratch as app

COPY --from=builder /go/src/app .

ENTRYPOINT [ "./main" ]
