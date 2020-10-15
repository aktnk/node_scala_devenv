# node_scala_devenv

Dockerfile and docker-compose.yml for the development of the Node.js and Scala.

## Usage

1. Set up the .env file
    * NODE_DOCKER_TAG : specify the tag of the official docker image of Node.js (https://hub.docker.com/_/node)
    * OPENJDK_TAG : specify the tag of the official docker image of OpenJDK (https://hub.docker.com/_/openjdk)
    * SBT_VERSION : specify the sbt version of the interactive build tool (https://www.scala-sbt.org/index.html)
    * SCALA_VERSION : specity the version of the Scala Prigramming language (https://www.scala-lang.org/) 
1. Build container image
    * run the docker-compose build command
    ```
    $ docker-compose build
    ```
1. Develop the application at the ./app directory
    * run the npm install command
    ```
    $ docker-compose run --rm nodedev npm install
    ```
    * run the npm run build command
    ```
    $ docker-compose run --rm nodedev npm run bild
    ```
    * run the sbt package command
    ```
    $ docker-compose run --rm sbtdev sbt package
    ```
## Reference

### Scala and sbt
* [Scala](https://www.scala-lang.org/)
* [Scala on GitHub](https://github.com/scala)
* [sbt:The interactive build tool](https://www.scala-sbt.org/index.html)

### Node.js
* [nodejs](https://nodejs.org/)
* [nodejs: Docker Official Images](https://hub.docker.com/_/node)
* [docker nodejs on GitHub](https://github.com/nodejs/docker-node)

### OpenJDK
* [openjdk: Docker Official Images](https://hub.docker.com/_/openjdk)
* [docker openjdk on GitHub](https://github.com/docker-library/openjdk)
