# Performant PHP on Kubernetes

This repo is used to demonstrate deploying a performant PHP application on Kubernetes.

It utilizes environment variables to allow you to configure OPcache and PHP-FPM to performance tune your containerized PHP application.

## Local Quick Start

### With Docker Compose
- Build and bring up all the containers up: `docker-compose up --build`

Visit `localhost:8080` in your browser to view current date. 

### Pushing to Docker Hub
- Build the PHP Docker image: `docker build -t <YOUR_USERNAME>/php-fpm .`
- Push it to Docker Hub: `docker push <YOUR_USERNAME>/php-fpm`

### Testing
- See the `php-fpm` config being used: `docker-compose exec app php-fpm -tt`
- See the php ini settings (including opcache) being used: `docker-compose exec app php-fpm -i`

## License

> This project is licensed under the terms of the MIT license.
