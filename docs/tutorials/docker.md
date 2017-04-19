# Development in Docker container

## For running the website directly from a container you can use docker : 

1. Install docker https://docs.docker.com/ (Follow the installation instructions for your platform)
2. Build the image `docker build -t realmapp .` and run the website with `docker run -it -p 3000:3000 -p 3001:3001 -v "$PWD":/app realmapp`  

## For specific dev commands, you can run those from container : 

Install all dependencies from docker command line :

    docker run -it -v "$PWD":/app realmapp npm install
    
Run the site from the container : 

    docker run -it -p 3000:3000 -p 3001:3001 -v "$PWD":/app realmapp npm run serve

Build the production version:

    docker run -it -v "$PWD":/app realmapp npm run build

For the explanation of the commands and their modifications please refer to https://docs.docker.com/engine/reference/run
