FROM ubuntu:18.04

EXPOSE 5000

WORKDIR /usr/src/app

COPY . .

RUN apt install nodejs && sudo apt install npm \
    npm install && npm install -g serve  \
    npm run build \
    useradd -m appuser && chown -R appuser:appuser ./build

ENV REACT_APP_BACKEND_URL=http://localhost:8080

USER appuser
 
CMD ["serve", "-s", "-l", "5000", "build"]
