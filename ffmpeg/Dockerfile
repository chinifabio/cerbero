FROM ubuntu:22.04

RUN apt update
RUN apt install -y ffmpeg

ENTRYPOINT ffmpeg \
-re \
-i ${RTSP_URL} \
-c:v libx264 \
-f flv \
-an \
-flush_packets 1 \
rtmp://nginx-container/streaming/cortile