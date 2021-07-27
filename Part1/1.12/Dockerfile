FROM node:14.17

EXPOSE 5000

WORKDIR /usr/src/app

RUN curl -sL https://deb.nodesource.com/setup_14.x | bash
RUN apt install -y nodejs

COPY . /usr/src/app

RUN node -v && npm -v

RUN ls -a

RUN npm install

RUN npm run build

RUN npm install -g serve

CMD ["serve", "-s", "-l", "5000", "build"]FROM node:14.17

