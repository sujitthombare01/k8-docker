FROM node:18
RUN apt update
RUN apt install git -y
RUN git clone https://github.com/sujitthombare01/hapi-server.git
WORKDIR hapi-server
RUN npm install
CMD node server.js
EXPOSE 8080