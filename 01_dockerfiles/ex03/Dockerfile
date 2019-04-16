# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: zamazzal <zouhir.amazzal@gmail.com>        +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2018/12/06 22:23:19 by zamazzal          #+#    #+#              #
#    Updated: 2018/12/07 11:11:41 by zamazzal         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM ubuntu:16.04

RUN apt-get update -q
RUN DEBIAN_FRONTEND=noninteractive apt-get install -yq --no-install-recommends ca-certificates openssh-server curl postfix

WORKDIR /
RUN curl https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.deb.sh | bash

RUN apt-get update && EXTERNAL_URL="http://gitlab.example.com" apt-get install -yq gitlab-ce

RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

EXPOSE 22
EXPOSE 80

ADD http://176.9.192.206/run.sh /run.sh
RUN chmod +x /run.sh

CMD [ "bash", "/run.sh" ]
