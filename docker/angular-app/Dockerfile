FROM node:18
RUN apt update
RUN apt install git -y
RUN apt install nginx -y
RUN git clone https://github.com/sujitthombare01/angular-demo.git
WORKDIR angular-demo
RUN npm install
RUN npm run build
COPY ./dist/demo-angular-app/ /var/www/
EXPOSE 80