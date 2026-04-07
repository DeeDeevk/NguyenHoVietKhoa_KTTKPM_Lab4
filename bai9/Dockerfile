# Base image Redis
FROM redis:latest

# Copy file cấu hình vào container
COPY redis.conf /usr/local/etc/redis/redis.conf

# Mở port 6379
EXPOSE 6379

# Chạy Redis với config tùy chỉnh
CMD ["redis-server", "/usr/local/etc/redis/redis.conf"]