# Install Nginx Server
      sudo apt update
      sudo apt install nginx

# Install node and npm 

     curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash


    Now install version you want to use
         nvm install version_name
         nvm install v18
         nvm -vserion
         nvm use version_name
         nvm user 18

# Clone Your Project file

         sudo git clone your_repo_url
          
# Install Dependances

       npm intsll 

       sudo chmod +R (whomiam) /var/www/file

# Configrure your nginx server 

        server {

               root /var/www/html/RANTIKAFRONTEND/RantikaThakur/build;
               index index.html
               server_name your_domain_name your_IP_address;

          location / {
               root /var/www/html;
               index index.html index.htm;
             }
        
         location /api {
                   proxy_pass http://localhost:3000;
                   
                   proxy_http_version 1.1;
                   
                   proxy_set_header Upgrade $http_upgrade;
                   
                   proxy_set_header Connection 'upgrade';
                   
                   proxy_set_header Host $host;
                   
                   proxy_cache_bypass $http_upgrade;
               }
                         
          }
    
                                
   
