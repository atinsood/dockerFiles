#Create the container using

sudo docker build -t asood/supervisord .

#Start the docker container using 

docker run -p 0.0.0.0:49022:22 -p 0.0.0.0:49080:80 -t -i asood/supervisord
Make sure that the ports 49080 and 49022 are exposed in vagrant
