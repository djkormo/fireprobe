FROM python:3.8-slim

# Get and install required packages.
RUN apt-get update && apt-get install -y -q \
    wget \
    net-tools \
    vim

# add Python OpenSSL package
RUN pip install --upgrade pip
RUN pip install pyOpenSSL

# env clean
RUN apt-get clean autoclean
RUN apt-get autoremove --yes
RUN rm -rf /var/lib/{apt,dpkg,cache,log}/

# app install
ENV APP_DIR /app
RUN mkdir -p $APP_DIR
WORKDIR $APP_DIR

RUN wget http://www.fireprobe.net/fireprobe.tar.gz
RUN tar -xf fireprobe.tar.gz
RUN rm -f fireprobe.tar.gz
RUN chmod +x fireprobe.sh
RUN rm -f install.sh

EXPOSE 9113
EXPOSE 9114

# EXEC python fireprobe
CMD python3 /app/bin/fireprobe.cpython-38.pyc -d 0 -p 9113 -s 1 -ps 9114 -l 1 --autoupdate 0 --selfcheck 0
