In the month of March 2020 Vimal Daga sir provide us great opportunty to learn something new and explore ourself.One of the technolgy they introduce is Docker.I had training on docker technology where I learnt lots of things under the guidance of Mr. Vimal Daga sir , now we are concluding this training so I have made this project for implementing whatever we have learnt in the 24 hours online class.We learnt lots of new things.As a beginner I havn't knowledge about the docker but due to this session i can handle a docker project.This is a project along with my experience while learning docker whatever problems I faced how I resolved them is provided here.
1. System Requirenments :
 For the project I need any operting system.vitually I can use either window or linux.I used linux for this project.
2. Docker Installation :
First of all copy the path of url from where we are going to install docker https://download.docker.com/linux/centos/7/x86_64/stable/ I would suggest go through this URL for installation. In the RHEL I have configure yum for installing community eddition of Docker.
I faced one problem where my docker container was unable to run as security system was refusing so I have got the solution while qna setenforce 0 this will turn of security enforcement.
3. Downloading Images :
This is very simple task we just have to pull images of os from https://hub.docker.com/ I have used centos image for configuring my webserver as well as a client .
https://hub.docker.com/_/centos this is the official image provided by centos we can pull this image by docker pull centos this command
4. Server creation :
I have launched one centos image in my container using docker run -it centos:latest command.
for configuration of webserver I have installed some softwares. First of all I was going to deploy my website on apache webserver so I have downloaded required softwares.
for installing apache webserver there are 3 steps
Software installation using yum install httpd
Deploying webpages inside /var/www/html folder
Start services using systemctl start httpd.services but in docker container systemctl process doesn't initializes so we have using yum install httpd I have installed software for webserver.
5. Website Deployment :
Now I have to deploy my website on apache webserver as I have mentioned earlier we have keep all the data that we have in /var/www/html folder
I have keep my webpages and other data in my computer system i used this to copy on given location
Now we are all set with website deployment now we just have to start service.
6. Configuration for automatically starting server on booting the image :
During this i faced some problem like, as server connected it shows only  connection but not the web pages.so I have to refresh it.But by simple killall command I unable to refresh server then I used to stop all apache server and again run it.
7. Image Creation using commit :
Now as I have configure normal centos according to my requirenment and I have to save it so we have an option called commit. docker container commit [OPTIONS] container [REPOSITORY : VERSION]
8. Start container using precreated image :
now as we have created our own image now we can multiply this as many times we want and can make as many servers we want in just few seconds.
9. Docker Compose :
Compose is a tool for defining and running multi-container Docker applications. With Compose, you use a YAML file to configure your application’s services.
Start, stop, and rebuild services
View the status of running services
Stream the log output of running services
Run a one-off command on a service
We have to create file docker-compose.yml this name should always be same.
Then we have some more options like in one click we can build whole infrastructure using docker-compose up command.
To stop services temporary we have docker-compose stop
To start stopped services we have docker-compose start
To destroy whole infrastructure we have docker-compose down

This was all about my learning in 3 weekends. I would like to thank Mr. Vimal Daga Sir for this great opportunity of learning.
