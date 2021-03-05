FROM golang:alpine3.13 as builder

WORKDIR /app

COPY ./codeeducation.go /app


RUN go build codeeducation.go

FROM scratch

COPY --from=builder /app /app
ENTRYPOINT ["/app/codeeducation"]

