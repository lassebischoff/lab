# A pattern for building images that works for most shell-based applications:
# 1. Start with a base image
# 2. Install packages
# 3. Copy scripts
# 4. Make them executable
# 5. Set the default command

FROM ubuntu:24:04

# Install dependencies
RUN apt-get update && \
		apt-get install -y --no-install-recommends curl jq && \
		rm -rf /var/lib/apt/lists/* # Remove chached apt repos to keep images smaller

WORKDIR /app

# Copy scripts
COPY start process .
RUN chmod +x start process

CMD ["./start"]
