# [Working with the Apache Maven registry](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-apache-maven-registry)

| Keyword | Description |
| --- | --- | 
| [USER_NAME] | 계정 이름 |
| [USER_TOKEN] | 계정 토큰 |
| [NAMESPACE] | 개인 계정 또는 조직의 이름 |
| [REPOSITORY] |  REPOSITORY |
| [GROUP] |  groupId |
| [ARTIFACT] |  artifactId |
| [VERSION] |  version |

# Setting

### ~.m2/settings.xml

```xml
<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0"
      xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
      xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0
                          http://maven.apache.org/xsd/settings-1.0.0.xsd">

  <activeProfiles>
    <activeProfile>github</activeProfile>
  </activeProfiles>

  <profiles>
    <profile>
      <id>github</id>
      <repositories>
        <repository>
          <id>central</id>
          <url>https://repo1.maven.org/maven2</url>
        </repository>
        <repository>
          <id>github</id>
          <url>https://maven.pkg.github.com/[NAMESPACE]/[REPOSITORY]</url>
          <snapshots>
            <enabled>true</enabled>
          </snapshots>
        </repository>
      </repositories>
    </profile>
  </profiles> 

  <servers>
    <server>
      <id>github</id>
      <username>[USER_NAME]</username>
      <password>[USER_TOKEN]</password>
    </server>
  </servers>

</settings>

```


# Publishing

### pom.xml
```xml
.
.
	<groupId>[GROUP]</groupId>
	<artifactId>[ARTIFACT]</artifactId>
	<version>[VERSION]</version>
.
.
  <distributionManagement>
    <repository>
      <id>github</id>
      <url>https://maven.pkg.github.com/[NAMESPACE]/[REPOSITORY]</url>
    </repository>
  </distributionManagement>
.
.
.
```

```bash
mvn deploy
```

# Installing

### pom.xml
```xml
.
.
  <dependency>
    <groupId>[GROUP]</groupId>
    <artifactId>[ARTIFACT]</artifactId>
    <version>[VERSION]</version>
  </dependency>
.
.
```

```bash
mvn install
```
