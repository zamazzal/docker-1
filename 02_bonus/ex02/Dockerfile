# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: zamazzal <zouhir.amazzal@gmail.com>        +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2018/12/06 22:47:28 by zamazzal          #+#    #+#              #
#    Updated: 2018/12/06 23:22:43 by zamazzal         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM ubuntu

RUN apt update
RUN apt upgrade -y
RUN apt install -y ssh
RUN apt install -y vsftpd
RUN apt install -y apache2
RUN cp /etc/vsftpd.conf /etc/vsftpd.conf.orig

COPY ./web /var/www/html

EXPOSE 80
EXPOSE 22
EXPOSE 21

CMD ["service", "apache2", "start"]
