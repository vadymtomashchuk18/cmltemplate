# cmltemplate

## Usage
Use this template as a base for your Spring Boot app @ CML

### Run
```bash
curl -sSL "https://raw.githubusercontent.com/CMLTeam/cmltemplate/master/init.sh?$(date +%T)" | bash
```

and follow instructions. 

The project folder with scaffolded code will be created in current folder. 

### Analyze with CML SonarQube instance
First, log into [SonarQube UI](https://sonar.cmlteam.com) and generate an access token for the project.
Then, run this command in project root folder:
```bash
mvn clean verify sonar:sonar -Dsonar-login-token=TOKEN
```                                                    

### Update mvnw

```
./mvnw -N io.takari:maven:0.7.7:wrapper
```  

### Swagger

Swagger UI available at http://localhost:8080/swagger-ui/index.html 


### MySQL

Connect via CLI:
```
docker exec -it mysql8 mysql cmltemplate -ucmltemplate -pcmltemplate
``` 

### Enable global CORS

Run either with `--cors.enabled=true` program argument OR with `CORS_ENABLED=true` environment variable. 