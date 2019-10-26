# devops-demo
devops-demo - CI/CD setup

#Install Nexus in Ubuntu

Download Nexus

$cd /opt

$ sudo wget https://sonatype-download.global.ssl.fastly.net/repository/repositoryManager/3/nexus-3.16.1-02-unix.tar.gz

$ sudo tar -zxvf nexus-3.16.1-02-unix.tar.gz

$ sudo mv /opt/nexus-3.16.1-02 /opt/nexus

As a good security practice, it is not advised to run nexus service as root. so create a new user called nexus and grant sudo access to manage nexus services.

$ sudo adduser nexus

Set no password for nexus user and enter below command to edit sudo file

$sudo visudo

Add the below line and Save. nexus ALL=(ALL) NOPASSWD: ALL

Change file and owner permission for nexus files

$ sudo chown -R nexus:nexus /opt/nexus
$ sudo chown -R nexus:nexus /opt/sonatype-work

Add nexus as a service at boot time

Open /opt/nexus/bin/nexus.rc file, uncomment run_as_user parameter and set it as following.

$ sudo vim /opt/nexus/bin/nexus.rc

run_as_user="nexus" (file shold have only this line)

Add nexus as a service at boot time

$ sudo ln -s /opt/nexus/bin/nexus /etc/init.d/nexus

Log in as a nexus user and start service

$ su - nexus
$ /etc/init.d/nexus start

check the port is running or not using netstat command

$ sudo netstat -plnt

allow the port 8081 and access the nexus http://:8081 login as a min default username and password is admin/admin123

