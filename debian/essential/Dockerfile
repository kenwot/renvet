# docker build -t renvet:debess .

FROM renvet:deb

LABEL maintainer="Kenown <kenown@msn.com>" \
    name="Venvet" \
    version="debess" \
    description="Debian 12 (bookworm) with build-essential"

RUN apt-get update \
    && apt-get install -y build-essential
