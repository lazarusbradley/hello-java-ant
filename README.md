# hello-java-ant
Compiling Hello-Java Using Ant in Jenkins

-Prerequisites: Jenkins should have - Ant Integration plugin and ant installed in host.
``yum install ant``

-Repo Reference: https://github.com/prasanjit-/hello-java-ant


```sh
-Build Steps:
export JAVA_HOME='/usr/lib/jvm/java-1.8.0-openjdk/'
ant compile jar run
```
