# syntax=docker/dockerfile:1
FROM nvidia/cuda:12.9.0-cudnn-devel-ubuntu24.04

# Install essential packages
RUN apt-get update && \
    apt-get install -y --no-install-recommends \
        build-essential \
        gdb \
        cmake \
        ninja-build \
        git \
        curl \
        wget \
        && rm -rf /var/lib/apt/lists/*

# Set up a default user (root for now, as in your config)
USER root
