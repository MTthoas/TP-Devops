# Stage 1: Build the application
FROM golang:1.17 as builder

WORKDIR /app
COPY . .
RUN go build -o main .

# Stage 2: Run the application
FROM golang:1.17

WORKDIR /app
COPY --from=builder /app/main .

EXPOSE 8080
CMD ["./main"]
