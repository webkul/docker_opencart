# docker_opencart
Pull Image from DockerHub :-

docker pull webkul/opencart

Run a container of this image using the following command :-

"docker run -d -p 80:80 -p 3306:3306 webkul/opencart:latest"

Note-: No other services should be running on port 80 and 3306 of your host system. If so, change ports in the above docker command.

In order to access the credentials of your database, you have to get the container's console. Run the following command :-

"docker exec -it $container_id bash"

You are supposed to run "docker ps" to know container's id before you run the above command. Within container,read the content of the file named password.txt to access your mysql database username and password by running :-

cat /password.txt

Once your mysql username and password is known to you, you can simply login to mysql and create database accordingly.
