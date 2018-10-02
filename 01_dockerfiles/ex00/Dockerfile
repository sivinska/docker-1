FROM alpine
RUN apk update && apk upgrade && apk add vim
ENTRYPOINT vim

#to build a docker file: docker build -t <give any name> .
#to verify if it worked: docker run -it --rm <the given name>
#to check created images: docker image ls
