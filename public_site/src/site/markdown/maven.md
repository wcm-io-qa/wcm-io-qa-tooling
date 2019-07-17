## Maven Repositories

### wcm.io Repository

The released wcm.io artifacts are available at Maven Central:

https://search.maven.org/search?q=io.wcm.qa

Snapshots releases are available on the Sonatype snapshot repository - use at your own risk!

https://oss.sonatype.org/content/repositories/snapshots/

The maven artifact coordinates are documented on the index page of each wcm.io module.


### Apache Snapshot Repository

Sometimes snapshot are referenced from the Apache Snapshot repository:

```xml
<repository>
  <id>apache-snapshots</id>
  <url>https://repository.apache.org/snapshots</url>
  <layout>default</layout>
  <releases>
    <enabled>false</enabled>
  </releases>
  <snapshots>
    <enabled>true</enabled>
    <updatePolicy>always</updatePolicy>
  </snapshots>
</repository>
```


### wcm.io Intermediate Release Repository

This repository is hosted on wcm.io and provides intermediate releses with revision number from snapshots from the Apache SCM trunk which are not officially released currently. They are replaced with the official versions as soon as they are released by the Apache project.

```xml
<repository>
  <id>wcm-io-apache-intermediate-release</id>
  <url>https://wcm.io/maven/repositories/apache-intermediate-release</url>
  <layout>default</layout>
  <releases>
    <enabled>true</enabled>
    <updatePolicy>never</updatePolicy>
  </releases>
  <snapshots>
    <enabled>false</enabled>
  </snapshots>
</repository>

<pluginRepository>
  <id>wcm-io-apache-intermediate-release</id>
  <url>https://wcm.io/maven/repositories/apache-intermediate-release</url>
  <releases>
    <enabled>true</enabled>
    <updatePolicy>never</updatePolicy>
  </releases>
  <snapshots>
    <enabled>false</enabled>
  </snapshots>
</pluginRepository>

```
