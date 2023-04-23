
## steps :
https://labs.play-with-docker.com/

    docker run -d -p 8080:8080 -u 0 jenkins/jenkins:lts-jdk11 # as root
    docker ps -a #copy container ID
    docker exec -it <containerid> bash
    cat /var/jenkins_home/secrets/initialAdminPassword #copy password
    
