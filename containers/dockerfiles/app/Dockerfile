FROM ubuntu:24.04 

# Install packages
RUN apt-get update && apt-get upgrade -y curl

# Create a data directory
RUN mkdir -p /app/data

# Download a file
RUN curl -o /app/data/file.txt https://example.com/file.txt

WORKDIR /app

COPY greet .

CMD ["./greet"]
