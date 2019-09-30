# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: kskostyl <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2019/09/24 19:00:08 by kskostyl          #+#    #+#              #
#    Updated: 2019/09/25 18:56:43 by kskostyl         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

#
# From an alpine image you’ll add to your container your favorite text editor, vim or emacs, that will launch along with your container.
# To build the Dockerfile you can use the command -> docker build --tag ex00 ./ .
# To test it we can simply run it with -> docker run --interactive --tty ex00
# 1. Let's pull the latest image from alpine.

FROM alpine:latest

# 2. We'll install some packages after upgrading.

RUN apk update && apk upgrade && apk add vim && apk add git && apk add gcc

# 3. We'll set up some environment variables to test in with our editor

ENV MY_NAME="ksenia"
ENV MY_EMAIL="ksenia@42.us.org"
ENV MY_WELCOME_MESSAGE="Welcome to vim.  you are now inside vim text-editor"

# 4. Let's echo the ENV variables into a .txt file 

RUN echo $MY_WELCOME_MESSAGE >> welcome.txt && echo $MY_NAME >> welcome.txt && echo $MY_EMAIL >> welcome.txt

# 5. We'll start our container inside vim in the welcome.txt file

ENTRYPOINT ["vim", "welcome.txt"]
