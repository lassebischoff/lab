# Stage 1: Generate HTML
FROM ubuntu:24.04 AS builder

WORKDIR /build
COPY generate-status .
# Run the script - Only adds one layer, because it is on one line
RUN chmod +x generate-status && ./generate-status > index.html

# Stage 2: Serve with nginx (unprivileged)
FROM nginxinc/nginx-unprivileged:1.28

# Copy the result (index.html) from the build stage (named builder) and copy to a directory
COPY --from=builder /build/index.html /usr/share/nginx/html/index.html

EXPOSE 8080
