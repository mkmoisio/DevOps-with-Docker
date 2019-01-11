FROM ubuntu:16.04

EXPOSE 5000
WORKDIR /home
COPY frontend-example-docker .
RUN apt-get update && apt-get install -y curl \
&& curl -sL https://deb.nodesource.com/setup_10.x | bash \
&& apt-get install -y nodejs \
&& npm install \
&& apt-get purge -y --auto-remove curl \
&& rm -rf /var/lib/apt/lists/*

CMD API_URL=http://localhost:8000 npm start;
