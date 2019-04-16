# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: zamazzal <zouhir.amazzal@gmail.com>        +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2018/12/07 01:36:03 by zamazzal          #+#    #+#              #
#    Updated: 2018/12/07 11:11:14 by zamazzal         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM ruby

RUN apt-get update
RUN apt-get upgrade -y
RUN gem install rails
RUN apt install nodejs -y

ONBUILD COPY . /opt/app
ONBUILD WORKDIR /opt/app

ONBUILD RUN bundle install
ONBUILD RUN rails db:migrate
ONBUILD RUN rails db:seed
