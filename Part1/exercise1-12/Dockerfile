FROM ubuntu:20.04

WORKDIR usr/src/app

EXPOSE 5000

COPY . .

RUN apt-get update && apt-get install curl -y

RUN curl -sL https://deb.nodesource.com/setup_14.x | bash && apt install -y nodejs

RUN npm install && npm run build && npm install -g serve

CMD ["serve", "-s", "-l", "5000", "build"]
