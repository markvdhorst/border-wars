## Border Wars
This is the base repository for the Border Wars application. It contains instructions and a docker-compose 
to build and run the application.

### Docker compose
Docker-compose can be used to bring up the frontend, backend and database at once.
This requires either the repositories to be present or empty folders to satisfy the build context while downloading 
images from the docker hub 


#### Build and run the application from source code
Clone the source code as subdirectories of this project

    git clone git@github.com:markvdhorst/border-wars-frontend.git border-wars-frontend
    git clone git@github.com:markvdhorst/border-wars-backend.git border-wars-backend

Build and run the application

    docker-compose build
    docker-compose up

#### Using images from dockerhub

Create the empty build directories to satisfy the docker-compose build context. This is required even with the --no-build flag.

    mkdir border-wars-frontend
    mkdir border-wars-backend
    
Run the application with docker-compose

    docker-compose pull
    docker-compose up --no-build
