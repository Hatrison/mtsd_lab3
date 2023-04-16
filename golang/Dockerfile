FROM golang:1.19 AS builder

WORKDIR /app

COPY . .

RUN CGO_ENABLED=0 go build -o build/fizzbuzz

FROM scratch

COPY --from=builder /app/build/fizzbuzz /fizzbuzz

COPY --from=builder /app/templates /templates

EXPOSE 8080

CMD ["/fizzbuzz", "serve"]