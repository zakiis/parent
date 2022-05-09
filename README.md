# Introduction

Zakiis - A public java framework  based on spring boot for enhancing your project or quick start a new project. 

# Quick start

We highly recommend using spring boot 2.x and spring cloud 3.x in your project. If these requirement can't meet, It's safe not using the features provided by Netflix  like Feign, Ribbon.

If your project don't have parent or you are going to create a new project, we recommend you using zakiis-parent as your project parent.

```xml
<project xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd" xmlns="http://maven.apache.org/POM/4.0.0"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
  <parent>
    <groupId>io.github.zakiis</groupId>
    <artifactId>zakiis-parent</artifactId>
    <version>0.0.4</version>
  </parent>
</project>
```

# Modules

It  consists of the following module:

- parent 
- common
- security
- spring
- job
- starter
- kettle
- mybatis-generator
- test

## parent

Manage the common part of this framework like jar version, plugins, distribution, repositories, sign, etc. Zakiis framework now using spring boot 2.6.4 and spring cloud 3.1.1. 

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

Integrated quartz with spring boot and provide a quartz service class to interact with quartz, you can add this to your project dependency if you have timed task requirement.

## mybatis generator

Used for generating mapper, model class and XML file about database table.

## test

test project for zakiis framework and shows how to integrated it into spring boot project.