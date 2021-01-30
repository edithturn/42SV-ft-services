FROM alpine

LABEL maintainer="Edith Puclla <epuclla@student.42.us.org>"

RUN apk add --update nginx && rm -rf /var/cache/apk/*

RUN mkdir -p /tmp/nginx/client-body

COPY srcs/nginx.conf /etc/nginx/nginx.conf
copy srcs/default.conf /etc/nginx/conf.d/default.conf

#copy website /urs/share/nginx/html

CMD ["nginx", "-g", "daemon off;"]