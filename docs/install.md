# Installation Guide

!!! warning "Note"
    This installation requires **docker**, **docker-compose**, and **git** be installed on your 
    server

!!! danger
    ServiceBot requires https in order to make api calls with Stripe live mode (test mode will still work),
    Ensure to have a cert on your server if you want to use this in production. 
    
##Steps

1. Ensure docker, docker-compose, and git are installed
2. Do a git clone of the deployment 


    ``git clone  good repo``
    
3. create the app with docker-compose


    ``docker-compose up -d``

4. Access the server with web browser, by default on port 80

5. Enter setup information, if SSL is not setup yet then make sure stripe keys are on test mode

6. Your ServiceBot should be ready to go!