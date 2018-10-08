FROM alpine
RUN apk update && apk upgrade && apk add vim
ENTRYPOINT vim

#to build a docker file: docker build -t ex00 .
#to verify if it worked: docker run -it --rm ex00
#to check created images: docker image ls
