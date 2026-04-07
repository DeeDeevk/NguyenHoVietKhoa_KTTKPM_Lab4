# Base image
FROM python:3.9

# Tạo thư mục làm việc
WORKDIR /app

# Copy source code
COPY app.py .

# Đặt biến môi trường
ENV APP_ENV=development

# Chạy ứng dụng
CMD ["python", "app.py"]