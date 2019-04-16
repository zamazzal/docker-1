# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: zamazzal <zouhir.amazzal@gmail.com>        +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2018/12/06 08:16:35 by zamazzal          #+#    #+#              #
#    Updated: 2018/12/06 23:23:57 by zamazzal         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM debian:8

RUN apt update
RUN apt upgrade -y
RUN apt install openjdk-7-jdk -y
RUN apt install default-jdk -y
RUN apt install screen -y
RUN apt install wget -y
RUN mkdir /home/minecraft

WORKDIR /home/minecraft
RUN wget -O minecraft_server.jar https://s3.amazonaws.com/Minecraft.Download/versions/1.11.2/minecraft_server.1.11.2.jar
RUN echo "eula=true" > eula.txt
RUN echo -e "config your server and use to run the server:" > how-to-run.txt
RUN echo "java -Xmx1024M -Xms1024M -jar minecraft_server.jar nogui" >> how-to-run.txt

EXPOSE 25565/tcp
EXPOSE 25565/udp
