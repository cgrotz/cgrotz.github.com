---
layout: post
category : Javascript
tagline: "rhino-maven-plugin 1.0.1 released"
tags : [Maven, Javascript, Mozilla Rhino]
---
*rhino-maven-plugin* is a Maven plugin to compile Javascript to Java class file using Mozilla Rhino. The compiled classes require Mozilla Rhino to run. The plugin is licensed under the Mozilla Public License 2.0 due to MPL being the license for Rhino

Maven Distribution
{code}
<build>
  <plugins>
    <plugin>
      <groupId>de.skiptag</groupId>
      <artifactId>rhino-maven-plugin</artifactId>
      <version>1.0.1</version>
    </plugin>
  </plugins>
</build>
{code}
You can start the compilation be simply calling
{code}
mvn rhino:compile
{code}
or by adding the following to the plugin tag:
{code}
<executions>
<execution>
<phase>compile</phase>
<goals>
<goal>compile</goal>
</goals>
</execution>
</executions>
{code}
Mozilla Rhino as dependency
{code}
<dependency>
<groupId>org.mozilla</groupId>
<artifactId>rhino</artifactId>
<version>1.7R4</version>
</dependency>
{code}
The artifact is deployed to Maven Central so no repository configuration should be necessary.
