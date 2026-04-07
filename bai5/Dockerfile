# ===== Stage 1: Build =====
FROM golang:1.21-alpine AS builder

WORKDIR /app

COPY . .

RUN go mod init app || true
RUN go mod tidy

# Build binary
RUN go build -o main .


# ===== Stage 2: Run =====
FROM alpine:latest

WORKDIR /root/

# Copy binary từ stage build
COPY --from=builder /app/main .

# Mở port 8080
EXPOSE 8080

# Chạy app
CMD ["./main"]