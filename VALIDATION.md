# Validation

This revision combines QA qualification and SQA regression/approval into one unified QA/SQA stage.

Validated in the packaging environment:

- Main Java sources compile successfully with `javac --release 8`.
- `pom.xml`, `qa-sqa-tests/pom.xml`, and `config/settings-jfrog.xml.example` are valid XML.
- All Ansible YAML files parse successfully.
- Architecture and release-flow Graphviz sources render successfully.
- Jenkinsfile contains one `QA / SQA Qualification and Approval` stage; the old separate QA-only and SQA approval stages are absent.
- Jenkinsfile references the renamed `qa-sqa-tests/` qualification project.
- The source tree contains no generated Maven `target/` or build directories.

Not executable in this packaging environment:

- Maven (`mvn` is not installed), so Surefire/Failsafe and `mvn deploy` must be run in your lab.
- Jenkins pipeline execution.
- Authenticated JFrog Artifactory publication/promotion.
- Ansible deployment to your QA/production hosts.
- Docker build/run.

Use `MANUAL-COMMANDS.md` to validate those stages in your lab before relying on the Jenkinsfile unchanged.
