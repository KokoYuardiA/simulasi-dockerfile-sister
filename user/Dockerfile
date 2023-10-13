FROM golang:1.18-alpine

RUN mkdir /app

RUN addgroup -S kokogroup
RUN adduser -S -D -h /app kokouser kokogroup
RUN chown -R kokouser:kokogroup /app
USER kokouser

COPY main.go /app

EXPOSE 8080
CMD go run /app/main.go