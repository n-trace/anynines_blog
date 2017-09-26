docker build -t own_image .

docker run -t -i own_image /bin/bash

fly --target example login --concourse-url http://localhost:8080

fly -t example set-pipeline -p docker-images-pipeline -c pipeline.yml -l credentials.yml

fly -t example unpause-pipeline -p docker-images-pipeline


