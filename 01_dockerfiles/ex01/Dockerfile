# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: zamazzal <zouhir.amazzal@gmail.com>        +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2018/12/06 03:47:42 by zamazzal          #+#    #+#              #
#    Updated: 2018/12/07 11:11:05 by zamazzal         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM debian

WORKDIR /home/
RUN apt update
RUN apt upgrade -y
RUN apt install bzip2 -y
RUN apt install tar -y
RUN apt install wget -y
RUN wget https://files.teamspeak-services.com/releases/server/3.5.0/teamspeak3-server_linux_amd64-3.5.0.tar.bz2
RUN tar -xf teamspeak3-server_linux_amd64-3.5.0.tar.bz2
RUN rm teamspeak3-server_linux_amd64-3.5.0.tar.bz2
RUN touch /home/teamspeak3-server_linux_amd64/.ts3server_license_accepted

EXPOSE 9987/udp
EXPOSE 30033/tcp
EXPOSE 10011/tcp
EXPOSE 41144/tcp
WORKDIR /home/teamspeak3-server_linux_amd64/
CMD ["sh", "/home/teamspeak3-server_linux_amd64/ts3server_minimal_runscript.sh", "start"]
