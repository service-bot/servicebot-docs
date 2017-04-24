# Installation Guide

!!! warning "Note"
    This installation requires **docker**, **docker-compose**, and **git** be installed on your 
    server

!!! danger
    ServiceBot requires https in order to make api calls with Stripe live mode (test mode will still work),
    Ensure to have a cert on your server if you want to use this in production. 
    
##Steps

1. Install docker if not installed already

    
    ``sudo wget -qO- https://get.docker.com/ | sh``

2. Install docker-compose


    ``sudo curl -o /usr/local/bin/docker-compose -L "https://github.com/docker/compose/releases/download/1.11.2/docker-compose-$(uname -s)-$(uname -m)"``

3. Do a git clone of the deployment 


    ``git clone  good repo``
    
4. Add SMTP email settings to the docker-compose if mail notifications are desired
    
5. create the app with docker-compose


    ``docker-compose up -d``

6. Access the server with web browser, by default on port 80

7. Enter setup information, if SSL is not setup yet then make sure stripe keys are on test mode

8. Your ServiceBot should be ready to go!