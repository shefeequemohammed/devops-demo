# devops-demo
devops-demo - CI/CD setup

OS - Ubuntu 16.04

1) Install Java
  sudo apt-get update
  sudo apt-get install openjdk-8-jdk

Now setup the JAVA_HOME. Check the installation directory
find /usr/lib/jvm/java-1.8* | head -n 3

open bash_profile

vi ~/.bash_profile


JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk-1.8.0.212.b04-1.el8_0.x86_64
export JAVA_HOME
PATH=$PATH:$JAVA_HOME
