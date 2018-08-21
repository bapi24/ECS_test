# containerization

docker -- platform
dockerfile

## setup docker on EC2

* launch ec2 instance and ssh into it
* update installed packages
    `sudo yum update -y`
* sudo install git
* install docker
    `sudo yum install -y docker`
* start docker service
    `sudo service docker start`
* add the ec2-user to the docker group:
    `sudo usermod -a -G docker ec2-user`
* command for docker installation verfication:
    `docker info`


## container registry

* goto ECS page on AWS console
* create container registry
* ssh into docker instance
* clone test repo
    `git clone https://github.com/awslabs/ecs-demo-php-simple-app`
* ls -al
* examine docker file
    `cat dockerfile`


## Build docker image

* command to build docker image
    `docker build -t docker-test-b24`
* command to check docker images currently present on EC2
    `docker images`
* run new docker image
    `docker run -p 80:80 docker-test-b24`


 
