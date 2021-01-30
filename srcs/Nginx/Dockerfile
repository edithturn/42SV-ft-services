FROM alpine

LABEL maintainer="Edith Puclla <epuclla@student.42.us.org>"

RUN apt-get update -y &&\
		apt-get install nano vim dialog apt-utils -y &&\
		apt-get install curl -y &&\
		apt-get install nginx -y

RUN apt-get clean && rm -rf /var/lib/apt/lists/*

COPY srcs /tmp/

CMD bash ./tmp/setup_application.sh