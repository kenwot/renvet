# docker build -t renvet:debpy .

FROM renvet:debess

RUN apt-get update \
    && apt-get install -y zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libsqlite3-dev libreadline-dev libffi-dev libbz2-dev \
    && cd ~ && wget https://www.python.org/ftp/python/2.7.18/Python-2.7.18.tgz && tar xf Python-2.7.18.tgz && cd Python-2.7.18 \
    && mkdir /usr/local/python2 && ./configure --prefix=/usr/local/python2 && make && make install \
    && ln -s /usr/local/python2/bin/python /usr/bin/python && ln -s /usr/local/python2/bin/python2 /usr/bin/python2 \
    && cd ~ && wget https://bootstrap.pypa.io/pip/2.7/get-pip.py && python2 get-pip.py \
    && ln -s /usr/local/python2/bin/pip /usr/bin/pip && ln -s /usr/local/python2/bin/pip2 /usr/bin/pip2 \
    && cd ~ && wget https://www.python.org/ftp/python/3.11.4/Python-3.11.4.tgz && tar xf Python-3.11.4.tgz && cd Python-3.11.4 \
    && mkdir /usr/local/python3 && ./configure --prefix=/usr/local/python3 && make && make install \
    && ln -s /usr/local/python3/bin/python3 /usr/bin/python3 && ln -s /usr/local/python3/bin/pip3 /usr/bin/pip3 \
    && rm -rf ~/*

