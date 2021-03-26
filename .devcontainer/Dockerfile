# '''Dockerfile for using Ubuntu18.04'''

# Set Ubuntu 18.04 as the base image.
FROM ubuntu:18.04

# Disable interactive installation.
ENV DEBIAN_FRONTEND=noninteractive

# Describe the packages to be installed at build time.
RUN apt update && apt upgrade -y && \
    apt install -y git \
    tzdata

# Set time zone to Asia/Tokyo
ENV TZ=Asia/Tokyo

# Setting the Japanese Locale
RUN apt install -y locales && \
    locale-gen ja_JP.UTF-8
ENV LANG ja_JP.UTF-8
ENV LANGUAGE ja_JP:ja
ENV LC_ALL=ja_JP.UTF-8
RUN localedef -f UTF-8 -i ja_JP ja_JP.utf8

# Metadata description.
LABEL maintainer="https://twitter.com/AIRO28_" \
    version="1.0" \
    description="Ubuntu18.04 container"

# Instructions to be executed at container startups.
CMD ["/bin/bash"]
