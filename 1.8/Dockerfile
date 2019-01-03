FROM ubuntu:16.04


EXPOSE 3001
ENV NODE_ENV=production
RUN apt-get update && apt-get install curl -y
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash && apt-get install -y nodejs
COPY kurssikartta-back /
RUN npm install
CMD npm start
