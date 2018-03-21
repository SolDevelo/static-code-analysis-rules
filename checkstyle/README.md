# Checkstyle

This is the Checkstyle ruleset we endorse for all of our Java projects. Built for Checkstyle version 8.


## Usage

To include Checkstyle in a Maven build, use the following configuration:

```xml
<plugin>
    <groupId>org.apache.maven.plugins</groupId>
    <artifactId>maven-checkstyle-plugin</artifactId>
    <version>2.17</version>
    <executions>
        <execution>
            <id>checkstyle</id>
            <phase>prepare-package</phase>
            <goals>
                <goal>checkstyle</goal>
            </goals>
        </execution>
    </executions>
    <dependencies>
        <dependency>
            <groupId>com.puppycrawl.tools</groupId>
            <artifactId>checkstyle</artifactId>
            <version>8.0</version>
        </dependency>
    </dependencies>
    <configuration>
        <consoleOutput>true</consoleOutput>
        <failsOnError>true</failsOnError>
        <configLocation>checkstyle.xml</configLocation>
    </configuration>
</plugin>
```
