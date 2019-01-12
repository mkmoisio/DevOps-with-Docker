FROM node:alpine

EXPOSE 8000

COPY backend-example-docker /

RUN adduser -D app
RUN npm install

RUN chown -R app:app /node_modules

USER app


CMD FRONT_URL=http://localhost:5000 npm start
