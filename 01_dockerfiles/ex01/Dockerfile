#https://www.diffen.com/difference/TCP_vs_UDP
#There are two types of Internet Protocol (IP) traffic. They are TCP or Transmission Control Protocol and UDP or User Datagram Protocol.
#TCP is connection oriented – once a connection is established, data can be sent bidirectional. 
#UDP is a simpler, connectionless Internet protocol. Multiple messages are sent as packets in chunks using UDP.
#
#
#wget retrieves content from web servers
#link and usage for teamspeak: https://www.vultr.com/docs/how-to-install-teamspeak-3-server-on-debian-9-stretch
#to extract bz2 file you need to install bzip2 (https://stackoverflow.com/questions/26958741/extract-tar-the-tar-bz2-file-error)



FROM debian

EXPOSE 9987/udp
EXPOSE 30033/tcp
EXPOSE 10011/tcp

RUN apt-get upgrade && apt-get update -y && apt-get install -y wget && apt-get install -y bzip2
RUN wget http://dl.4players.de/ts/releases/3.4.0/teamspeak3-server_linux_amd64-3.4.0.tar.bz2
RUN tar xvf teamspeak3-server_linux_amd64-3.4.0.tar.bz2

WORKDIR teamspeak3-server_linux_amd64
RUN touch .ts3server_license_accepted

ENTRYPOINT sh ts3server_minimal_runscript.sh
