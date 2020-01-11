
## setup mysql container

      # copy image with required version
      docker pull mysql/mysql-server:5.7.28-1.1.13

      #run the server image
      docker run -p 3306:3306 --name=dbserver -d <image_id>

      # wait till container is healthy
      docker ps

      # copy temp password from the logs
      docker logs dbserver
      docker logs observer 2>&1 | grep GENERATED

      # set new password
      docker exec -it observer mysql -uroot -p
      mysql> ALTER USER 'root'@'localhost' IDENTIFIED BY ‘<new password>’;

      # give access from any host 
      select host, user from mysql.user;
      update mysql.user set host='%' where user = 'root';

      # update config
      docker exec -it observer bash
      yum install vim-enhanced
      vim /etc/my.cnf
      max_allowed_packet=64M
      bind-address=0.0.0.0

      # restart container
      docker container restart <id>

      # access shell 
      docker exec -it dbserver bash

### useful docker commands

      # list of stopped containers
      docker container ls -f "status=exited"

