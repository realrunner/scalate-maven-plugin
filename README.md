scalate-maven-plugin
====================

A [Maven][1] plugin for pre-compiling [Scalate][2] templates.

history
---
March 2020. Support for scala 2.13
This plugin was separated from the main [scalate repository][3] in March 2015.
This plugin was forked from `"org.scalatra.scalate" % "maven-scalate-plugin_2.11" % "1.7.1"` to add support for scala 2.12


Usage
---

```
pom.xml

<dependencies>
	<dependency>
	    <groupId>org.scalatra.scalate</groupId>
	    <artifactId>scalate-core_2.12</artifactId>
	    <version>1.8.0</version>
	</dependency>

	<dependency>
	    <groupId>org.scalatra.scalate</groupId>
	    <artifactId>scalate-spring-mvc_2.12</artifactId>
	    <version>1.8.0</version>
	</dependency>
</dependencies>

<build>
	<plugins>
		<plugin>
		  <groupId>com.stephenn</groupId>
		  <artifactId>maven-scalate-plugin_2.12</artifactId>
		  <version>0.0.1</version>
		  <executions>
		    <execution>
		      <phase>test-compile</phase>
		      <goals>
		        <goal>precompile</goal>
		      </goals>
		    </execution>
		  </executions>
		</plugin>
	</plugins>
</build>

```


Publishing
---

```
GPG_TTY=$(tty)
export GPG_TTY
mvn deploy -DperformRelease=true -Dgpg.keyname= -Dmaven.javadoc.skip=true
```

[1]: http://maven.apache.org
[2]: http://scalate.github.io/scalate
[3]: https://github.com/scalate/scalate