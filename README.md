# docker-gradle

# Create Docker Image
Do the following when creating an docker image.
```
% make build
```
Can be executed by specifying the Gradle version.
For example, execute it for the Gradle=6.4.1 version. 
```
% make build gradle_version=6.4.1 ostype=centos7 javatype=oracle jdk_ver=jdk8
```

# Execute Gradle Build
Do the following when executing Gradle build.
```
% make run src=[Target Source] cmd=[Target Command]
```

Can be executed by specifying the Gradle version.
For example, execute it for the "Project" folder. 
```
% make run src=Project cmd="gradlew" gradle_version=6.4.1 ostype=centos7 javatype=oracle jdk_ver=jdk8
```

# Points to remember
Gradle repository cache does not remain because Docker container is deleted after build.
Therefore, it takes build time each time.
If this becomes a problem, it needs to be improved.

