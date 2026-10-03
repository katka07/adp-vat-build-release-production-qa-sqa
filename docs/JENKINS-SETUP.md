# Jenkins Setup Required by Jenkinsfile

Configure these Jenkins tools:

```text
JDK tool name:   jdk8
Maven tool name: maven-3.8
```

Install/configure plugins used by the Jenkinsfile:

```text
Pipeline / Declarative Pipeline
Credentials Binding
SSH Agent
JUnit
SonarQube Scanner for Jenkins
```

Install these command-line tools on the release agent:

```text
git
docker
ansible
jf (JFrog CLI)
sha256sum
```

Create Jenkins credentials:

```text
jfrog-vat-ci   Username with password/token credential
vat-deploy-ssh SSH private-key credential for QA/Production hosts
```

Configure these non-secret global environment variables on the Jenkins agent/folder/job:

```text
JFROG_URL
JFROG_MAVEN_VIRTUAL_REPO
JFROG_SNAPSHOT_REPO
JFROG_CANDIDATE_REPO
JFROG_PRODUCTION_REPO
```

Configure the SonarQube server in Jenkins with the name:

```text
sonarqube
```

The example inventory uses RFC 5737 documentation addresses. Replace them with your lab hosts before deployment.
