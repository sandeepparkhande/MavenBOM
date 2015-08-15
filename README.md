# MavenBOM
Maven Poc

Added  Bom Dependency in POC

<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
	<modelVersion>4.0.0</modelVersion>
	<groupId>BoMPoc</groupId>
	<artifactId>BoMPoc</artifactId>
	<version>0.0.1-SNAPSHOT</version>
    <packaging>pom</packaging>
    
	<dependencyManagement>
		<dependencies>
			<dependency>
				<groupId>org.springframework</groupId>
				<artifactId>spring-framework-bom</artifactId>
				<version>4.0.1.RELEASE</version>
				<type>pom</type>
				<scope>import</scope>
			</dependency>
		</dependencies>
	</dependencyManagement>

</project>


Injected Bom Dependency in Client project

<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
	<modelVersion>4.0.0</modelVersion>

	<parent>
		<groupId>BoMPoc</groupId>
		<artifactId>BoMPoc</artifactId>
		<version>0.0.1-SNAPSHOT</version>
	</parent>
	<groupId>BoMClient</groupId>
	<artifactId>BoMClient</artifactId>
	<packaging>jar</packaging>
	<version>0.0.1-SNAPSHOT</version>

	<dependencies>
		<dependency>
			<groupId>org.springframework</groupId>
			<artifactId>spring-context</artifactId>
		</dependency>
		<dependency>
			<groupId>org.springframework</groupId>
			<artifactId>spring-web</artifactId>
		</dependency>
	</dependencies>
	
</project>

See Depedency injected in Classpath 4.0.1.RELEASE for Spring jars

<?xml version="1.0" encoding="UTF-8"?>
<classpath>
  <classpathentry kind="src" path="src/test/java" output="target/test-classes" including="**/*.java"/>
  <classpathentry kind="src" path="src/test/resources" output="target/test-classes" excluding="**/*.java"/>
  <classpathentry kind="src" path="src/main/java" including="**/*.java"/>
  <classpathentry kind="src" path="src/main/resources" excluding="**/*.java"/>
  <classpathentry kind="output" path="target/classes"/>
  <classpathentry kind="con" path="org.eclipse.jdt.launching.JRE_CONTAINER"/>
  <classpathentry kind="var" path="M2_REPO/org/springframework/spring-context/4.0.1.RELEASE/spring-context-4.0.1.RELEASE.jar"/>
  <classpathentry kind="var" path="M2_REPO/org/springframework/spring-aop/4.0.1.RELEASE/spring-aop-4.0.1.RELEASE.jar"/>
  <classpathentry kind="var" path="M2_REPO/aopalliance/aopalliance/1.0/aopalliance-1.0.jar"/>
  <classpathentry kind="var" path="M2_REPO/org/springframework/spring-beans/4.0.1.RELEASE/spring-beans-4.0.1.RELEASE.jar"/>
  <classpathentry kind="var" path="M2_REPO/org/springframework/spring-core/4.0.1.RELEASE/spring-core-4.0.1.RELEASE.jar"/>
  <classpathentry kind="var" path="M2_REPO/commons-logging/commons-logging/1.1.1/commons-logging-1.1.1.jar"/>
  <classpathentry kind="var" path="M2_REPO/org/springframework/spring-expression/4.0.1.RELEASE/spring-expression-4.0.1.RELEASE.jar"/>
  <classpathentry kind="var" path="M2_REPO/org/springframework/spring-web/4.0.1.RELEASE/spring-web-4.0.1.RELEASE.jar"/>
</classpath>


