# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: kskostyl <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2019/09/24 19:29:11 by kskostyl          #+#    #+#              #
#    Updated: 2019/09/24 19:35:28 by kskostyl         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

#
# This is a bonus to be able to get emacs dockerized with a simple welcome.txt project.
# You can test this project by: 
# 1. Building the image first docker build -t emacs .
# 2. Running the container in interactive and tty mode docker run --interactive --tty emacs
#

FROM debian:latest

# We update, upgrade and install all the necessary packets for emcas and friends

RUN  apt-get update -y && apt-get upgrade -y && apt-get install emacs -y && apt-get install git -y && apt-get install gcc -y

# We setup some environment variables that we can cat into our welcome.txt file

ENV MY_NAME="ksenia"
ENV MY_EMAIL="ksenia@42.us.org"
ENV MY_WELCOME_MESSAGE="Welcome to Emacs text-editor"

# We add some text into the welcome.txt file

RUN echo $MY_WELCOME_MESSAGE >> welcome.txt && echo $MY_NAME >> welcome.txt && echo $MY_EMAIL >> welcome.txt

# We start the container in bash mode

CMD ["bash"]
