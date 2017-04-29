# Installation Guide

!!! warning "Note"
    This installation requires **docker**, **docker-compose**, and **git** be installed on your 
    server

!!! danger
    ServiceBot requires https in order to make api calls with Stripe live mode (test mode will still work),
    Ensure to have a cert on your server if you want to use this in production.

        Certificates should be named as follows and placed in a single folder
        not publically accessible on the host system:
        - Keyfile : servicebot.key
        - Certificate : servicebot.crt
        - CA : servicebot_bundle.crt
        
    
##Steps

####1. Install docker if not installed already
        
    sudo wget -qO- https://get.docker.com/ | sh
        
####2. Install docker-compose
        
    sudo curl -o /usr/local/bin/docker-compose -L "https://github.com/docker/compose/releases/download/1.11.2/docker-compose-$(uname -s)-$(uname -m)"

####3. Do a git clone of the deployment 

     git clone https://github.com/service-bot/servicebot-deploy.git
    
####4. Create a folder on the server and place SSL Certificate files in it

    Certificates should be named as follows:
    - Keyfile : servicebot.key
    - Certificate : servicebot.crt
    - CA : servicebot_bundle.crt



####5. Configure docker-compose.yaml File

For SMTP: Edit and uncomment the following lines to match your SMTP server information
 
    SMTP_HOST : "localhost"
    SMTP_USER : "postmaster@localhost"
    SMTP_PASSWORD : "password"
    SMTP_PORT : "587"

For SSL: uncomment the two SSL lines and change /path/to/ssl/certs/on/server
to the path on your server that you created for the certificates
     
      CERTIFICATES: "./ssl/"
      - /path/to/ssl/certs/on/server:/usr/src/app/ssl


####6. Build Images
    
    docker-compose build

####7. Start containers in the background:
    
    docker-compose up -d
    
####8. Access the server with web browser
      
####9. Input Stripe Keys

####10. Input admin account information


  
## Helpful commands
####Restarting all containers:
    
    docker-compose restart
####View logs from all services:
    
    docker-compose logs
