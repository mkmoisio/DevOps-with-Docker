FROM ubuntu:16.04

RUN apt-get update && apt-get install -y python wget ffmpeg \
&& apt-get install -y python-pip python-dev build-essential \
&& pip install --user --upgrade yle-dl \
&& apt-get purge -y --auto-remove python-pip \
&& apt-get purge -y --auto-remove python-dev \
&& apt-get purge -y --auto-remove build-essential \
&& apt-get install --reinstall python-pkg-resources \
&& rm -rf /var/lib/apt/lists/*


WORKDIR /app

ENTRYPOINT ["/root/.local/bin/yle-dl"]
