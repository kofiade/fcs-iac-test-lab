# =============================================================
# INTENTIONALLY INSECURE DOCKERFILE — FOR TESTING ONLY
# =============================================================

# CRITICAL: Using 'latest' tag — unpinned and non-reproducible
FROM ubuntu:latest

# CRITICAL: Running as root (no USER directive)
# CRITICAL: Using ADD instead of COPY (ADD can unpack remote URLs)

# Install packages without version pinning
RUN apt-get update && apt-get install -y \
    curl \
    wget \
    netcat-openbsd \
    ssh \
    telnet

# CRITICAL: Hardcoded secret in environment variable
ENV DATABASE_PASSWORD="SuperSecret123!"
ENV API_KEY="AKIAIOSFODNN7EXAMPLE"

# CRITICAL: Exposing too many ports including SSH
EXPOSE 22 80 443 3306 5432 8080 9090

# CRITICAL: No HEALTHCHECK defined
# CRITICAL: Running as root (never switched to non-root user)

CMD ["bash"]
