FROM node:alpine3.11

EXPOSE 5000

WORKDIR /usr/src/app

COPY . .

ENV REACT_APP_BACKEND_URL=http://localhost:8080

RUN npm install && npm install -g serve \
    && npm run build && adduser -S userapp \ 

USER userapp
 
CMD ["serve", "-s", "-l", "5000", "build"]
