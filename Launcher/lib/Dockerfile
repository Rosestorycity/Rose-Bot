FROM node:lts-buster

RUN git clone https://github.com/Rosestorycity/Rose-Bot  /root/rose

RUN apt-get update && \
apt-get install -y \
ffmpeg \
webp && \
apt-get upgrade -y && \
rm -rf /var/lib/apt/lists/*

WORKDIR /root/rose

ENV TZ=Asia/Kolkata

RUN npm install

RUN npm install supervisor -g
RUN yarn install --ignore-engines
CMD ["node", "index.js"]
