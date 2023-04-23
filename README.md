
## steps :
https://labs.play-with-docker.com/
### Pre-Req

    docker run -d -p 8080:8080 -u 0 jenkins/jenkins:lts-jdk11 # as root
    docker ps -a #copy container ID
    docker exec -it <containerid> bash
    cat /var/jenkins_home/secrets/initialAdminPassword #copy password
    
Steps:
- In docker-playground page click on link "8080"
- Install all default addons
- Paste above password when asked 
- Skip the rest of the steps 
- Jenkins Home 
- New Item > Name "test" >Select  FreeStype Project > Ok
- Select "GitHub project"
- Source Code Management > "Git"
- Repo Url "https://github.com/j-thepac/HelloWorld.git"
- Branch "main"
- Build Steps > Execute Shell
- Select either of the below code 

## Java
    java -version
    javac helloworld.java
    java helloworld

## Python 
    apt-get -y update
    apt-get install -y python3 
    python3 helloworld.py
