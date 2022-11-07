1) git clone https://github.com/RetmixX/Settings_environment
2) Select one of the assemblies and run docker-compose
  1.1) If select dev, setting .env file:
      DATABASE_NAME=*you data base name*
      DATABASE_USER=*you database user*
      DATABASE_PASSWORD=*you database password*
      
   1.2) execute command docker-compose -f docker-compose.dev.yaml up
   
   2.1) If select prod, setting .env file
   
   2.2) execute command docker-compose -f docker-compose.prod.yaml up
