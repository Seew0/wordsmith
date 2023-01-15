#building and running go file
FROM golang:1.19-alpine as builder

WORKDIR /home/app

COPY dispatcher.go .

RUN go build dispatcher.go

CMD [ "/dispatcher" ] 

# starting a web server
FROM nginx:1.23.2-alpine as web 

COPY static /usr/share/nginx/html

EXPOSE 80

