FROM ubuntu:16.04

EXPOSE 5000
RUN apt-get update && apt-get install curl -y
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash && apt-get install -y nodejs
COPY frontend-example-docker /home
RUN cd home/ && npm install
CMD cd home/; API_URL=http://localhost:8000/ npm start;
