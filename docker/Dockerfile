FROM nginx:alpine
RUN apk update && apk add 
COPY ./index.html /usr/share/nginx/html/
EXPOSE 80
ENTRYPOINT ["nginx", "-g", "daemon off;"]
