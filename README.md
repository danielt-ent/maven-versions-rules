# Maven Versions Plugin Rules

default rules to ignore common unwanted maven version patterns like  -RC -M1 etc
cf. https://www.mojohaus.org/versions-maven-plugin/version-rules.html

To use, take the following config:

```xml
	<build>
		<plugins>
			<plugin>
				<groupId>org.codehaus.mojo</groupId>
				<artifactId>versions-maven-plugin</artifactId>
				<dependencies>
					<dependency>
						<groupId>me.dtem</groupId>
						<artifactId>maven-versions-rules</artifactId>
						<version>1.0.0</version>
					</dependency>
				</dependencies>
				<configuration>
					<rulesUri>classpath:///versions-rules.xml</rulesUri>
				</configuration>
			</plugin>
		</plugins>
	</build>
	<pluginRepositories>
		<pluginRepository>
			<id>github</id>
			<name>GitHub Packages</name>
			<url>https://maven.pkg.github.com/danielt-ent/maven-versions-rules</url>
		</pluginRepository>
	</pluginRepositories>
```