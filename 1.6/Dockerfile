FROM ubuntu:16.04

EXPOSE 8000
RUN apt-get update && apt-get install curl -y
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash && apt-get install -y nodejs
COPY backend-example-docker /
RUN npm install
CMD FRONT_URL=http://localhost:5000 npm start
