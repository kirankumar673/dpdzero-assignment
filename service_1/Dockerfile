FROM golang:1.22-alpine

WORKDIR /app

# Copy source code
COPY . .

# Build the binary and name it "service1"
RUN go build -o service1 main.go

# Expose the port
EXPOSE 8001

# Run the binary
CMD ["./service1"]