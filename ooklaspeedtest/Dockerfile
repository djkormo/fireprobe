#FROM ubuntu:bionic

#WORKDIR /var/www

#RUN apt-get update && \
#    apt-get install -y wget && \
#    rm -rf /var/lib/apt/lists/*

#RUN wget https://install.speedtest.net/ooklaserver/ooklaserver.sh && \
#    chmod a+x ooklaserver.sh && \
#    ./ooklaserver.sh install -f

# Expose the default port
#EXPOSE 8080 5060

#CMD ["./OoklaServer", "start"]

FROM debian:11.6

WORKDIR /var/www


RUN apt-get update && \
    apt-get install -y wget && \
    apt-get remove  -y sqlite3 && \
    rm -rf /var/lib/apt/lists/*

#RUN mkdir -p /usr/local/share/ca-certificates


RUN wget https://install.speedtest.net/ooklaserver/ooklaserver.sh && \
    chmod a+x ooklaserver.sh && \
    ./ooklaserver.sh install -f

# Expose the default port
EXPOSE 8080 5060

CMD ["./OoklaServer", "start"]
