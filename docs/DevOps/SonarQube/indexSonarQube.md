# Configuration of SonarQube and SonarScanner with Docker

## Windows

Install Docker Desktop

### Download SonarQube image from Docker Hub

´´´
docker pull sonarqube
´´´

Configure volume to persist data of the tool (you can create the volumes before to run the container)

Command to create a volume :

´´´
docker volume create name-volume
´´´

To check persistent of datas in repositories :

´´´
docker volume inspect name-volume
´´´

You can create symbolic links to an easier access location.

**OR**

´´´
docker run -d 
    --name sonarqube 
    -p 9000:9000 
    -p 9092:9092 
    -v sonarqube-conf:/opt/sonarqube/conf 
    -v sonarqube-data:/opt/sonarqube/data 
    -v sonarqube-logs:/opt/sonarqube/logs 
    -v sonarqube-extensions:/opt/sonarqube/extensions 
    sonarqube
´´´
## Run SonarScanner 

### Download with the Zip File

* [SonarScanner - Documentation](https://docs.sonarqube.org/latest/analysis/scan/sonarscanner/)

add in the **PATH** the link to sonar-scanner.bat, to use the keyword "sonar-scanner.bat"

´´´
sonar-scanner.bat -D"sonar.projectKey=project" -D"sonar.sources=." -D"sonar.host.url=http://localhost:9000" -D"sonar.login=09c098cc02bdb88f0de3af7b5aa4073574a008e8"
´´´

docker run --rm -e SONAR_HOST_URL="http://localhost:9000" -e SONAR_LOGIN="09c098cc02bdb88f0de3af7b5aa4073574a008e8" -v "C:\Tools:/usr/src" sonarsource/sonar-scanner-cli

docker run -it --name sonarscanner sonarsource/sonar-scanner-cli

docker run -it --link sonarqube newtmitch/sonar-scanner:4-alpine -D sonar.host.url=http://sonarqube:9000 -D sonar.scm.provider=git -D sonar.projectBaseDir=./src -D sonar.sources=. -D sonar.projectName='Test-Project'