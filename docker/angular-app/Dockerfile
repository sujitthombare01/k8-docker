#stage 1
FROM node:14.19 as node
RUN apt update
RUN apt install git -y
RUN git clone https://github.com/sujitthombare01/web-app.git
WORKDIR /web-app
RUN git checkout dev
COPY . .
RUN npm install
RUN npm run build
#stage 2
FROM nginx:alpine
COPY --from=node /web-app/dist /usr/share/nginx/html