jenkins-trigger-polling_triglav
===============================

# Description

Jenkins Plugin For [Triglav](https://github.com/sonots/triglav).

# Usage

![image](https://cloud.githubusercontent.com/assets/4525500/23051173/46e4e0fc-f50a-11e6-87c6-50b6098162dd.png)

- **Job Id (ReadOnly)**: Job id on Triglav. Users cannot configure this value.
- **Username**: Username to authenticate to Triglav.
- **Password**: Password to authenticate to Triglav.
- **Authenticator**: Authentication method to Triglav. Now just supporting `LOCAL` which means using user database on Triglav.
- **Api Key (ReadOnly)**: API Key which Triglav publishes. Users cannot configure this value.
- **Job Message Offset (ReadOnly)**: Job Message Offset which the job consumed. Users cannot configure this value.
- **Time Zone**: Time Zone of resources.
- **Time Unit**: Time Unit of resources.
- **Logical Operator**: Logical Operator for which Triglav uses in monitoring resources. `and` or `or` is available.
- **Resources**:
  - **Id (ReadOnly)**: Resource id on Triglav. Users cannot configure this value.
  - **URI**: Resource URI.

# Development

## Prepare Dependencies

Require the below.

- [triglav](https://github.com/sonots/triglav/blob/5cc95322b843993875211226a343940aa6d49e64/README.md)
- java
- gradle

## Build Jenkins for Debug

```
git clone git@github.com:civitaspo/jenkins-trigger-polling_triglav.git
cd jenkins-trigger-polling_triglav
./run-debug-server.sh
```

### Note: For Intellij IDEA Users

The feature of "break point" does not work on Intellij IDEA if you debug by `Gradle Task Debugger` (ref. https://github.com/jenkinsci/gradle-jpi-plugin).
Use `Remote Debugger` instead.

# Build Plugin

```
./gradlew jpi
```

This plugin is built into `build/libs/jenkins-trigger-polling_triglav.hpi`.

# Release Plugin

TBD

# TODO

- Remove Jobs & Resources correctly from [Triglav](https://github.com/sonots/triglav).
- Write tests.
- Write [Jenkins wiki](https://wiki.jenkins-ci.org/display/JENKINS/Plugins)
- Release to Public.

# Reference

- [Jenkins Plugin Development Reference](https://wiki.jenkins-ci.org/display/JENKINS/Extend+Jenkins)
- [Jenkins Unit Test](https://wiki.jenkins-ci.org/display/JENKINS/Unit+Test)
- [Jenkins Mocking in Unit Test](https://wiki.jenkins-ci.org/display/JENKINS/Mocking+in+Unit+Tests)
- [Jenkins Gradle JPI Plugin](https://github.com/jenkinsci/gradle-jpi-plugin)
- [Triglav API Document](https://github.com/sonots/triglav/tree/master/doc)
- [Triglav Java Client Document](https://github.com/sonots/triglav-client-java/tree/master/docs)