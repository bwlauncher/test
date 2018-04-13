FROM alpine

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
