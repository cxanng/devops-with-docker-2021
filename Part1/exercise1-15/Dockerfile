FROM ubuntu:20.04

WORKDIR usr/src/app

EXPOSE 3000

RUN apt update && apt install curl -y

RUN curl -fsSL https://deb.nodesource.com/setup_15.x | bash -E -

RUN apt install nodejs -y

COPY . .

RUN npm install

CMD ["npm", "start"]