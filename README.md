# Introduction

Zakiis - A public java framework  based on spring boot for enhancing your project or quick start a new project. 

# Quick start

We highly recommend using spring boot 2.x and spring cloud 3.x in your project. If these requirement can't meet, It's safe not using the features provided by Netflix  like Feign, Ribbon.

We recommend using our BOM (bill of materials)

```xml
<dependencyManagement>
  <dependencies>
    <dependency>
      <groupId>io.github.zakiis</groupId>
      <artifactId>zakiis-dependencies</artifactId>
      <version>0.0.4</version>
      <scope>import</scope>
      <type>pom</type>
    </dependency>
  </dependencies>
</dependencyManagement>
```

sample pom file for spring boot web application

```xml
<project xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd" xmlns="http://maven.apache.org/POM/4.0.0"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
  <modelVersion>4.0.0</modelVersion>
  <groupId></groupId>
  <artifactId></artifactId>
  <version>0.0.4</version>
  
  <name></name>
  <url></url>
  <description></description>
  
  <properties>
    <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
    <java.version>1.8</java.version>
  </properties>
  
  <dependencyManagement>
    <dependencies>
      <dependency>
        <groupId>io.github.zakiis</groupId>
        <artifactId>zakiis-dependencies</artifactId>
        <version>0.0.4</version>
        <scope>import</scope>
        <type>pom</type>
      </dependency>
    </dependencies>
  </dependencyManagement>
    
  <dependencies>
    <!-- if you are using zakiis-starter -->
    <dependency>
      <groupId>io.github.zakiis</groupId>
      <artifactId>zakiis-starter</artifactId>
    </dependency>
    <dependency>
	  <groupId>org.springframework.boot</groupId>
	  <artifactId>spring-boot-starter</artifactId>
	</dependency>
    <dependency>
	  <groupId>org.springframework.boot</groupId>
	  <artifactId>spring-boot-starter-test</artifactId>
	  <scope>test</scope>
	</dependency>
	
    <!-- if you are using spring web-->
    <dependency>
	  <groupId>org.springframework.boot</groupId>
      <artifactId>spring-boot-starter-web</artifactId>
    </dependency>
    <!-- if you are using open feign-->
    <dependency>
	  <groupId>org.springframework.cloud</groupId>
	  <artifactId>spring-cloud-starter-openfeign</artifactId>
    </dependency>
  </dependencies>
    
  <build>
    <plugins>
      <plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-compiler-plugin</artifactId>
        <version>3.8.1</version>
        <configuration>
          <source>${java.version}</source>
          <target>${java.version}</target>
          <parameters>true</parameters>
          </configuration>
      </plugin>
      <plugin>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-maven-plugin</artifactId>
        <version>2.6.4</version>
      </plugin>
    </plugins>
  </build>
</project>
```

# Modules

It  consists of the following module:

- parent 
- dependencies
- common
- security
- spring
- job
- starter
- kettle
- mybatis-generator
- workflow
- test

## parent

Manage the common part of this framework like jar version, plugins, distribution, repositories, sign, etc. Zakiis framework now using spring boot 2.6.4 and spring cloud 3.1.1. 

## dependencies

Dependencies BOM (Bill of Materials)

## common

Common Module contains util class that we used frequently and exception structure. click [here](https://github.com/zakiis/common/blob/main/README.md) to learn more.

## security

Security module contains some security util, like `AES`, `HMAC`, `RSA`, and some digest util like `MD5`, `SHA`, some codec util like `Hex`, `Base64`, some security solution like `JWT`, `log desensitization` , `authorization`。click [here]( https://github.com/zakiis/security/blob/main/README.md) to learn more.

## spring

Spring module provides some filter and interceptor that has tight relation to spring framework. For example: `http damboard`, `global trace id`, `mybatis cipher and log sql`, `web authorization`.

## starter

Used for spring boot starter, It provides some properties class and auto configuration class to make framework can auto loaded and configured in your project.

## kettle

Integrated kettle with spring boot and provide a kettle service class to execute your transform job, you can use this project to quick solving your ETL requirements.

## job

Integrated quartz with spring boot and provide a quartz service class to interact with quartz, you can add this to your project dependency if you have timed task requirement. click [here](https://github.com/zakiis/job/blob/main/README.md) to learn more

## mybatis generator

Used for generating mapper, model class and XML file about database table.

## Workflow

This module is designed for demonstrate the way of integration with [Activiti6](https://www.activiti.org/), Which is the well-known framework of BPMN2.0 implementation by java language.

more details could find  on [activiti official document](https://www.activiti.org/userguide/#_introduction), click [here](https://github.com/zakiis/workflow/blob/main/README.md) to learn more.

## test

test project for zakiis framework and shows how to integrated it into spring boot project.