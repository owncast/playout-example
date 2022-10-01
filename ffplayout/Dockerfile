FROM ubuntu:latest

ENV DEBIAN_FRONTEND=noninteractive

COPY ffplayout_0.15.2_amd64.deb /tmp

RUN apt update && apt-get install -y ffmpeg
RUN apt install -y /tmp/ffplayout_0.15.2_amd64.deb

EXPOSE 8787

CMD [ "/bin/ffplayout", "-i", "--log", "/logs", "--folder", "/video", "--play-mode", "folder", "--config", "/etc/ffplayout/ffplayout.yml"]