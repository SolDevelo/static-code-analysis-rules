# Checkstyle

This is the Checkstyle ruleset we endorse for all of our Java projects. Built for Checkstyle version 8.


## Usage

To include Checkstyle in a Maven build, use the following configuration:

```xml
<plugin>
    <groupId>org.apache.maven.plugins</groupId>
    <artifactId>maven-checkstyle-plugin</artifactId>
    <version>3.0.0</version>
    <executions>
        <execution>
            <id>checkstyle</id>
            <phase>prepare-package</phase>
            <goals>
                <goal>checkstyle</goal>
            </goals>
        </execution>
    </executions>
    <configuration>
        <consoleOutput>true</consoleOutput>
        <failsOnError>true</failsOnError>
        <configLocation>checkstyle.xml</configLocation>
        <sourceDirectories>${project.build.sourceDirectory}</sourceDirectories>
    </configuration>
</plugin>
```

`configLocation` point to the configuration file location (starting from app root directory)
`sourceDirectories` point to the directory that is going to be checked

Additionally, for most of Spring projects, you'll need a static main class, with default, public constructor.
In that case add ```@SuppressWarnings("checkstyle:hideutilityclassconstructor")``` above this main class, so it won't be
treated like a utility class.
