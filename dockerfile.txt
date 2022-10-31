
FROM nginx:alpine

COPY nginx.conf /etc/nginx/nginx.conf

WORKDIR /usr/share/nginx/html

RUN rm -rf ./*

COPY ./* ./

ENTRYPOINT ["nginx", "-g", "daemon off;"]