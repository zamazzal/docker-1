# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: zamazzal <zouhir.amazzal@gmail.com>        +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2018/12/06 21:08:45 by zamazzal          #+#    #+#              #
#    Updated: 2018/12/06 23:45:46 by zamazzal         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM debian

WORKDIR /home
RUN apt update
RUN apt install -y clamav
RUN apt install -y nmap
RUN apt install -y chkrootkit
RUN apt install -y fail2ban
RUN apt install -y ufw
RUN apt install -y iptables
RUN apt install -y ssh
RUN apt install -y netcat
RUN apt install -y aircrack-ng
RUN apt install -y hydra
RUN apt install -y yersinia
RUN apt install -y beef
RUN apt install -y hashcat
RUN apt install -y pixiewps

EXPOSE 22
