FROM golang:1.19 AS builder

WORKDIR /app

COPY go.mod go.sum ./

RUN go mod download

COPY . .

RUN go build -o build/fizzbuzz

FROM gcr.io/distroless/base

COPY --from=builder /app/build/fizzbuzz /

COPY --from=builder /app/templates /templates

EXPOSE 8080

CMD ["/fizzbuzz", "serve"]