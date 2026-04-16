FROM nginx:1.27-alpine

RUN apk update && apk upgrade --no-cache

COPY . /usr/share/nginx/html

EXPOSE 80

HEALTHCHECK CMD wget --no-verbose --tries=1 --spider http://localhost || exit 1