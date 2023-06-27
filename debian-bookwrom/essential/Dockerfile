# docker build -t renvet:bookworm.essential .

FROM renvet:bookworm

LABEL maintainer="Kenown <kenown@msn.com>" \
    name="Venvet Base Image" \
    version="bookwrom" \
    description="A Debian 12 (bookworm) base image for Renvet"

RUN apt-get update \
    && apt-get install -y build-essential
