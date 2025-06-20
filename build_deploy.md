# build
[https://github.com/spring-projects/spring-framework/wiki/Build-from-Source](https://github.com/spring-projects/spring-framework/wiki/Build-from-Source)

```bash
./gradlew build -x checkstyleMain -x checkstyleNohttp -x test
```

# deploy
```bash
./gradlew -PdeploymentRepository=${deploymentRepository} -PossrhUsername=${uername} -PossrhPassword=${password} publishAllPublicationsToDeploymentRepository -x test -x checkstyleMain -x checkstyleNohttp
```
e.g.
```bash
./gradlew -PdeploymentRepository=http://nexus.xxx.com/repository/xxx-release/ -PossrhUsername=xxx -PossrhPassword=xxxx build publishAllPublicationsToDeploymentRepository -x test -x checkstyleMain -x checkstyleNohttp
```
