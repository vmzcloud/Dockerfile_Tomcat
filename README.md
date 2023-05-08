<img src="https://img.shields.io/badge/language-Dockerfile-blue.svg"/> <img src="https://img.shields.io/github/last-commit/vmzcloud/Dockerfile_Tomcat"/><p>
<img src="https://img.shields.io/docker/v/vmzcloud/tomcat?color=yellow">
<img src="https://img.shields.io/docker/image-size/vmzcloud/tomcat?color=orange">

# Official website
<img src="https://tomcat.apache.org/res/images/tomcat.png"><p>
<a href="https://tomcat.apache.org/index.html" target="_blank">https://tomcat.apache.org/index.html</a><p>
<a href="https://archive.apache.org/dist/tomcat/tomcat-9/" target="_blank">Tomcat 9</a><p>
<a href="https://github.com/adoptium/temurin11-binaries/releases" target="_blank">OpenJDK</a>

# DockerHub
<a href="https://hub.docker.com/r/vmzcloud/tomcat" target="_blank">vmzcloud/tomcat</a><p>

# Build
<pre>
# docker build -f Dockerfile_Tomcat -t vmzcloud/tomcat:version .
</pre>
## Example:
<pre>
# docker build -f Dockerfile_Tomcat_9.0.74-openjdk_11.0.19_7-alpine -t vmzcloud/tomcat:9.0.74-openjdk_11.0.19_7-alpine .
</pre>

# Tomcat Configuration
<pre>
Remove webapps/docs
Remove webapps/example
</pre>

# Using docker
<pre>
docker run -d \
--name=tomcat \
-p 8080:8080 \
-v ${PWD}/webapps:/opt/tomcat/webapps \
--restart unless-stopped \
vmzcloud/tomcat:9.0.74-openjdk_11.0.19_7-alpine
</pre>

# Sample Application for Deploy Test
<a href="https://tomcat.apache.org/tomcat-7.0-doc/appdev/sample/" target="_blank">https://tomcat.apache.org/tomcat-7.0-doc/appdev/sample/</a><p>
Download the Sample Application (sample.war)<p>
Put the sample.war file into ${PWD}/webapps
