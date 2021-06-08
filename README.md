# need mysql8
```
cd docker
docker-compose up -d
```

# guide
- openjdk11 install for macos
```
brew tap AdoptOpenJDK/openjdk
brew install --cask adoptopenjdk11
```

# build native image
```
./gradlew build -Dquarkus.package.type=native -Dquarkus.native.container-build=true
docker build -f src/main/docker/Dockerfile.jvm -t example .
docker run --name example -i -d --rm example
```
