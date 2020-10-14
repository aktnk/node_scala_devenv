ARG OPENJDK_TAG
FROM openjdk:${OPENJDK_TAG}

# Install sbt
ARG SBT_VERSION
RUN \
  curl -L -o sbt-${SBT_VERSION}.deb https://dl.bintray.com/sbt/debian/sbt-${SBT_VERSION}.deb && \
  dpkg -i sbt-${SBT_VERSION}.deb && \
  rm sbt-${SBT_VERSION}.deb && \
  apt-get update && \
  apt-get install sbt

# Install Scala
ARG SCALA_VERSION
RUN \
  curl -fsL https://downloads.typesafe.com/scala/${SCALA_VERSION}/scala-${SCALA_VERSION}.tgz | tar xfz - -C /root/ && \
  echo "export PATH=~/scala-${SCALA_VERSION}/bin:$PATH" >> /root/.bashrc

RUN sbt sbtVersion
