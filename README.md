In this folder I build a docker image from the NGINX latest Image (check the Dockerfile for code) and added my static website to build my own image called myapp.
Code:
insert this in the Dockerfile of your website
FROM nginx:latest
ADD . /usr/share/nginx/html
Then run:
docker build --tag myapp:latest .

With this procedure, I was able to build my own imgae from Nginx and add my static website to replace the Nginx html path and avoid running my website with volumes.
