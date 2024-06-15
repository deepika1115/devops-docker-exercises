# Use the official golang image as the base image
FROM golang:1.16

# Set the Current Working Directory inside the container
WORKDIR /app

# Copy the source from the current directory to the Working Directory inside the container
COPY . .



# Build the project
RUN go build

# Test the project
RUN go test ./...

# Expose port 8080
EXPOSE 8080

# Command to run the executable
CMD ["./server"]