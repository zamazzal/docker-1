# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: zamazzal <zouhir.amazzal@gmail.com>        +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2018/12/06 07:51:14 by zamazzal          #+#    #+#              #
#    Updated: 2018/12/06 23:23:11 by zamazzal         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM debian

WORKDIR /home
RUN apt update
RUN apt -y upgrade
RUN apt install wget tar zip -y
RUN wget http://linux.mtasa.com/dl/multitheftauto_linux_x64.tar.gz
RUN tar -xf multitheftauto_linux_x64.tar.gz
RUN wget http://linux.mtasa.com/dl/baseconfig.tar.gz
RUN tar -xf baseconfig.tar.gz
RUN mv baseconfig/* multitheftauto_linux_x64/mods/deathmatch
RUN rm -rf baseconfig.tar.gz baseconfig multitheftauto_linux_x64.tar.gz

WORKDIR /home/multitheftauto_linux_x64
RUN mkdir mods/deathmatch/resources

WORKDIR /home/multitheftauto_linux_x64/mods/deathmatch/resources
RUN wget http://mirror.mtasa.com/mtasa/resources/mtasa-resources-latest.zip
RUN unzip mtasa-resources-latest.zip
RUN rm -f mtasa-resources-latest.zip

EXPOSE 22003/udp
EXPOSE 22005/tcp
EXPOSE 22126/udp

WORKDIR /home/multitheftauto_linux_x64
