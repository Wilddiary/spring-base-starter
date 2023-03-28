# spring-base-starter [![Release](https://github.com/Wilddiary/spring-base-starter/actions/workflows/maven-release.yml/badge.svg)](https://github.com/Wilddiary/spring-base-starter/actions/workflows/maven-release.yml)
A minimal service chassis for Spring micro-services. Includes a standard build experience and dependencies for distributed tracing and metrics collection. Allows faster bootstrapping of services.

Imports Spring boot and cloud dependencies. Does not include spring-boot-maven-plugin build plugin out of the box to allow use in Spring library applications too. Child projects that require an executable jar to be built, would need to include it as below.

```
<build>
  <plugins>
    <plugin>
      <groupId>org.springframework.boot</groupId>
      <artifactId>spring-boot-maven-plugin</artifactId>
      <version>${spring-boot-maven-plugin.version}</version>
      <executions>
        <execution>
          <goals>
            <goal>repackage</goal>
          </goals>
        </execution>
      </executions>
    </plugin>
  </plugins>
</build>
```

Includes GPG build plugin for signing the build artifacts. If you desire the artifacts should be signed then you need to configure GPG on your environment. Else, you can skip the signing process by setting the `gpg.skip` property to true either in your pom.xml or by passing it as a system property to maven.
