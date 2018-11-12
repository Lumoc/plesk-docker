# Dockerfiles for Plesk

Dockerfiles for building Plesk images.

# Ready to Use Images


Create a container based on published image for evaluation purposes:

    docker run -d -p 8880:8880 lumoc/docker-plesk

Use Docker host IP address and 8880 port for URL to open it in the browser. The following command can be used in the terminal:

    open http://`docker-machine ip`:8880
    
Default login and password: admin / changeme 

Create a container with typical port mapping:

    docker run -d -p 80:80 -p 443:443 -p 8880:8880 -p 8443:8443 -p 8447:8447  lumoc/docker-plesk

Automatic port mapping can be used to publish all exposed ports to random ports with the high numbers:

    docker run -d -P  lumoc/docker-plesk


