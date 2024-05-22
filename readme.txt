mkdir -p /Users/$(whoami)/jenkins_home

➜  k8s docker run -u 0 --privileged --name jenkins -it -d -p 8080:8080 -p 50000:50000 \ 
-v /var/run/docker.sock:/var/run/docker.sock \
-v $(which docker):/usr/bin/docker \
-v /Users/$(whoami)/jenkins_home:/var/jenkins_home \
jenkins/jenkins:latest

docker ps

docker logs -f ........
8aaf4cf6523440a18061d933ae445116
-- lấy mật khẩu đăng nhập lần đâu
localhost:8080/login
install suggested plugins
create first admin user
admin
12345678
admin
test@gmail.com

homepage>plugin manager>available>docker pipeline>tick>install without restart>go back to the top page
manage jenkins>manage plugin>available>kubernetes continous deploy> lỗi
>advanced>upload>kubernetes-cd.hpi 
https://updates.jenkins.io/download/p...
kiểm tra cài đặt trong >install>kubernetes continous deploy 1.0.0

https://github.com/shazforiot/nodeapp_test
