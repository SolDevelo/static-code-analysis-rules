# PMD

This is the PMD ruleset we endorse for all of our Java projects. Built for PMD version 6.1.0.

## Usage

To include PMD and CPD in a Maven build, use the following configuration:

```
<plugin>
    <groupId>org.apache.maven.plugins</groupId>
    <artifactId>maven-pmd-plugin</artifactId>
    <version>3.9.0</version>
    <executions>
        <execution>
            <phase>test</phase>
        </execution>
    </executions>
    <configuration>
        <analysisCache>true</analysisCache>
        <rulesets>
            <ruleset>pmd.xml</ruleset>
        </rulesets>
        <includeTests>true</includeTests>
        <minimumTokens>100</minimumTokens>
        <failOnViolation>true</failOnViolation>
    </configuration>
</plugin>
```
