FROM nginx:1.27-alpine

# update security patch
RUN apk update && apk upgrade --no-cache

# copy เฉพาะ web app
COPY app/ /usr/share/nginx/html

# ใช้ non-root user
USER nginx

EXPOSE 80

HEALTHCHECK CMD wget --no-verbose --tries=1 --spider http://localhost || exit 1