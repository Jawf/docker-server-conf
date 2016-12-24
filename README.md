##Docker server images common configuration for usual docker server:

Docker sample blog: http://blog.csdn.net/jawfneo/article/details/52518352

###mysql docker server:
>docker pull daocloud.io/library/mysql:5.7.15
>docker run -d --restart "always" --name "mysql" -v /home/data/mysql:/var/lib/mysql -v /home/application/mysql/my.cnf:/etc/mysql/my.cnf -e MYSQL_ROOT_PASSWORD=root daocloud.io/library/mysql:5.7.15

customised configuration which overwrite the one for /etc/mysql/my.cnf from: /home/applicaiton/mysql/my.conf

`Command to check character setting: 
docker exec -it mysql /bin/sh
mysql> show variables where variable_name like 'character_set%';
`

###spring boot application
//TODO

###nginx docker server
>docker pull daocloud.io/library/nginx:mainline 
>docker run -d --restart "always" --name "mysql" -p 80:80 -v /home/application/nginx/nginx.conf:/etc/nginx/nginx.conf ¨Clink=spring-boot-app:app-container daocloud.io/library/nginx:mainline

