# Base image with Python
FROM python:3.11-slim

# Set work directory
WORKDIR /app

# Copy app files
COPY . .

# Install Flask
RUN pip install flask

# Expose port
EXPOSE 8002

# Healthcheck
HEALTHCHECK --interval=30s --timeout=3s --start-period=10s --retries=3 \
  CMD curl --fail http://localhost:8002/ping || exit 1

# Run the app
CMD ["python", "app.py"]
