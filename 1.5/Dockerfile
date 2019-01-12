FROM node:alpine

EXPOSE 5000
WORKDIR /home
COPY frontend-example-docker .
RUN adduser -D app
RUN mkdir /home/dist \
&& chown -R app:app /home/dist
RUN npm install

USER app

CMD API_URL=http://localhost:8000 npm start;
