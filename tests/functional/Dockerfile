# This Dockerfile is used to build a Kamihi project environment for functional testing purposes.

# Use the Astral UV image with Python 3.12 and Debian Bookworm as the base image.
FROM ghcr.io/astral-sh/uv:python3.12-bookworm-slim@sha256:7fc7d030e69807610096804ffe498dff01419f5e6718cbc9ed2e2f7ea59729f2

# Copy the current local version of Kamihi to the image.
COPY . /lib/kamihi

# Add environment variables for future dependencies installation.
ENV UV_COMPILE_BYTECODE=1
ENV UV_LINK_MODE=copy
ENV PATH="/app/.venv/bin:$PATH"

# Sets the working directory to /app.
WORKDIR /app
