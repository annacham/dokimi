ubuntu@ubuntu-VirtualBox:~/Downloads/downloads$ sudo docker ps
CONTAINER ID   IMAGE                         COMMAND                  CREATED             STATUS          PORTS                                                  NAMES
4ce6271ad363   downloads_calculate-web-app   "/usr/bin/supervisord"   About an hour ago   Up 51 minutes   0.0.0.0:5000->5000/tcp, :::5000->5000/tcp              downloads_calculate-web-app_1
54d4d911ef59   mysql:latest                  "docker-entrypoint.s…"   About an hour ago   Up 51 minutes   0.0.0.0:3306->3306/tcp, :::3306->3306/tcp, 33060/tcp   downloads_mysql_1



sudo docker tag downloads_calculate-web-app annacham/calculate-web-app:latest
sudo docker tag mysql:latest annacham/mysql-container:latest



sudo docker push annacham/calculate-web-app:latest
sudo docker push annacham/mysql-container:latest


