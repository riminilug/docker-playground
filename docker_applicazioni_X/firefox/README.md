#Dockerfile

FROM ubuntu:14.04
RUN apt-get update && apt-get install -y firefox
CMD /usr/bin/firefox



#Build the container

docker build -t firefox .



#Run the container

export DISPLAY=YOUR-IP:0.0
docker run -ti --rm -e DISPLAY=$DISPLAY firefox
