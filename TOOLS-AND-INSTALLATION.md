# Tools and Installation

For the historical Java application use Java 8-compatible compilation. A practical lab needs:

```text
Git
JDK 8
Maven 3.5+ (3.8.x is convenient for the lab)
Docker Engine (optional runtime packaging)
Ansible
JFrog CLI
Graphviz (only to edit/render diagrams)
```

Jenkins agent additionally needs access to the QA/Production hosts by SSH and connectivity to JFrog and SonarQube.

Example Ubuntu packages where available:

```bash
sudo apt-get update
sudo apt-get install -y git ansible curl unzip ca-certificates
```

Install the JDK/Maven versions required by your lab or configure them as Jenkins managed tools. JFrog CLI and Docker should be installed from their vendor-supported repositories/packages for your operating system.

Verify:

```bash
java -version
mvn -version
ansible --version
jf --version
docker --version
```
