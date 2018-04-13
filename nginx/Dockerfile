FROM alpine
#RUN set -x ; \
#  addgroup -g 82 -S nginx ; \
#  adduser -u 82 -D -S -G nginx nginx && exit 0 ; exit 1

RUN apk update && \
    apk add nginx && \
    apk add nano 
RUN rm -rf /var/cache/apk/* 
#   chown -R nginx:nginx /var/lib/nginx

COPY nginx/nginx.conf /etc/nginx/nginx.conf
COPY nginx/conf.d/80.conf /etc/nginx/conf.d/80.conf
COPY nginx/conf.d/topremont.conf /etc/nginx/conf.d/topremont.conf

EXPOSE 4080 4443
CMD ["nginx", "-g", "daemon off;"]
