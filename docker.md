
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
      
### mongo db setup
    # create a volume
    # volumes are required to preseve data in case container fails
    docker volume create mongodbdata
    
    # pull the image
    docker pull mongo:4.2.1
    
    # run container
    docker run -d --restart=always --network=devnet --name=mongodb -p 27017-27019:27017-27019 -v mongodbdata:/data/db mongo:4.2.1
      
### docker network

      # create a docker network
      docker network create devnet
      
      # add containers to network, either by passing through run or while running
      docker network connect devnet app-container
      docker network connect devnet dbserver
      
      # from app-container
      ping dbserver // works, resolves to dbserver.devnet

### useful docker commands

      # list of stopped containers
      docker container ls -f "status=exited"
      
      # run container
      docker run -d --restart=always --network=devnet --name=webapp -p 0.0.0.0:8000:8000 webapp:0.2
      
      # rename container
      docker rename oldname newname
      
      # docker logs
      docker container logs webapp -f
      
      # built with specific file
      docker build -f testMode.Dockerfile -t webapp:0.1 .

### Links

      https://hub.docker.com/r/mysql/mysql-server/tags/?page=1&name=5.7
      https://hub.docker.com/r/mikemanger/python27-mysql
      https://dev.mysql.com/doc/mysql-installation-excerpt/5.5/en/docker-mysql-getting-started.html
      https://github.com/docker-library/mysql/issues/275
      
