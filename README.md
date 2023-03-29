<h1 style="text-align:center;font-weight: bold; margin-top: 20px; margin-bottom: 20px;">spring-base-starter </h1>

<p style="text-align:center;">

  <img alt="Github Build" src="https://img.shields.io/github/actions/workflow/status/Wilddiary/spring-base-starter/maven-release.yml" />
  <img alt="Synk Vulnerabilities" src="https://img.shields.io/snyk/vulnerabilities/github/Wilddiary/spring-base-starter" />
  <img alt="GitHub Language Count" src="https://img.shields.io/github/languages/count/Wilddiary/spring-base-starter" />
  <img alt="GitHub Top Language" src="https://img.shields.io/github/languages/top/Wilddiary/spring-base-starter" />
  <img alt="GitHub Repo Size" src="https://img.shields.io/github/repo-size/Wilddiary/spring-base-starter" />
  <img alt="GitHub File Count" src="https://img.shields.io/github/directory-file-count/Wilddiary/spring-base-starter" />
  <img alt="GitHub Issues" src="https://img.shields.io/github/issues/Wilddiary/spring-base-starter" />
  <img alt="GitHub Closed Issues" src="https://img.shields.io/github/issues-closed/Wilddiary/spring-base-starter" />
  <img alt="GitHub Pull Requests" src="https://img.shields.io/github/issues-pr/Wilddiary/spring-base-starter" />
  <img alt="GitHub Closed Pull Requests" src="https://img.shields.io/github/issues-pr-closed/Wilddiary/spring-base-starter" />
  <img alt="GitHub Release" src="https://img.shields.io/github/v/release/Wilddiary/spring-base-starter?date_order_by=created_at&sort=date" />
  <img alt="GitHub Tag" src="https://img.shields.io/github/v/tag/Wilddiary/spring-base-starter" />
  <img alt="GitHub Contributors" src="https://img.shields.io/github/contributors/Wilddiary/spring-base-starter" />
  <img alt="GitHub Last Commit" src="https://img.shields.io/github/last-commit/Wilddiary/spring-base-starter" />
  <img alt="GitHub Commit Activity (Week)" src="https://img.shields.io/github/commit-activity/w/Wilddiary/spring-base-starter" />
  <img alt="GitHub Commit Activity (Month)" src="https://img.shields.io/github/commit-activity/m/Wilddiary/spring-base-starter" />
  <img alt="GitHub Commit Activity (Year)" src="https://img.shields.io/github/commit-activity/y/Wilddiary/spring-base-starter" />
  <img alt="Github License" src="https://img.shields.io/github/license/Wilddiary/spring-base-starter" />
  <img alt="Forks" src="https://img.shields.io/github/forks/Wilddiary/spring-base-starter" />
  <img alt="Followers" src="https://img.shields.io/github/followers/Wilddiary" />
  <img alt="Discussions" src="https://img.shields.io/github/discussions/Wilddiary/spring-base-starter" />

</p>

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

