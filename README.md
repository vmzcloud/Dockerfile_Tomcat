# Docker Tomcat

<b>Build</b>
<pre># docker build -f Dockerfile_Tomcat -t vmzcloud/tomcat:version .</pre>

<b>Usage</b>
<pre># docker run -d -p 8080:8080 vmzcloud/tomcat:9.0.65-openjdk-11.0.16_8</pre>
<pre># docker run -d -p 8080:8080 vmzcloud/tomcat:8.5.82-openjdk-11.0.16_8</pre>

<b>Components</b>
<pre>
centos7
openjdk
apache-tomcat
</pre>

<b>Configuration</b>
<pre>
Remove webapps/docs
Remove webapps/examples
</pre>
