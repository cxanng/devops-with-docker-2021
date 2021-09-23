FROM ubuntu:20.04 


EXPOSE 8080

RUN apt-get update
RUN apt-get install -y wget git gcc

RUN wget -P /tmp https://dl.google.com/go/go1.17.1.linux-amd64.tar.gz

RUN tar -C /usr/local -xzf /tmp/go1.17.1.linux-amd64.tar.gz
RUN rm /tmp/go1.17.1.linux-amd64.tar.gz

ENV PATH $PATH:/usr/local/go/bin

WORKDIR /usr/local/go/bin

COPY . .

RUN go build

CMD ["./server"]