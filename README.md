# Docker-project
•	Description of my Docker project :-
•	Wordpress is an open source software which is used to create many kind of websites, blog or app.This is done with the help of docker on the top of Redhat 8 linux. After that I pulled the image of wordpress and mysql. Now it is very important that when ever any containers crash or get deleted, it should not damage my data. 
•	For this I have created new volume using command [docker volume create] create volume for both wordpress and mysql. 
•	Then I launched mysql container first with the volume I created, followed by wordpress.
•	For launching mysql container commad used is: 
    docker run -d -it -e MYSQL_ROOT_PASSWORD : somewordpress
    -e MYSQL_USER : wordpress
    -e MYSQL_PASSWORD : wordpress 
    -e MYSQL_DATABASE : wordpress
    -v mysql_storage : /var/lib/mysql 

•	Now for launching word press container we used command: 
       docker run -d -it -e WORDPRESS_DB_HOST : db:3306
       -e WORDPRESS_DB_USER : wordpress
       -e WORDPRESS_DB_PASSWORD : wordpress
       -e WORDPRESS_DB_NAME : wordpress
       -v wp_storage : /var/www/html

•	In order to avoid these steps again and again I created a docker-compose which contains all necessary steps written as code in yaml file with .yml extension. 
•	Then at last we can do "docker-compose up" in order to execute it. 
•	Check the logs to see that  everything is working fine. Configure IP.
•	Type the IP with port  in the browser to launch the wordpress.com
•	Wordpress will ask for configuration setup. Complete this setup and it is ready.



My first project under the guidance of Mr. Vimal Daga sir.
