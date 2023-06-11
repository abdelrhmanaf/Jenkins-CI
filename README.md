# Jenkinsfile

This is a Jenkinsfile for a pipeline that builds, tests, and deploys the vprofile-project.

## Prerequisites

To run this pipeline, you need the following tools installed on your Jenkins server:

- Maven
- SonarQube Scanner
- Nexus Repository Manager

## Pipeline Overview

This pipeline consists of the following stages:

1. **Fetch Code**: This stage fetches the code from the Git repository.

2. **BUILD**: This stage builds the code using Maven and archives the generated WAR file.

3. **UNIT TEST**: This stage runs unit tests using Maven.

4. **INTEGRATION TEST**: This stage runs integration tests using Maven.

5. **CODE ANALYSIS WITH CHECKSTYLE**: This stage runs Checkstyle to analyze the code.

6. **CODE ANALYSIS WITH SONARQUBE**: This stage runs SonarQube to analyze the code and generates a quality gate report.

7. **Publish to Nexus Repository Manager**: This stage uploads the generated WAR file to the Nexus Repository Manager.

## Environment Variables

This pipeline uses the following environment variables:

- `NEXUS_VERSION`: The version of the Nexus Repository Manager.
- `NEXUS_PROTOCOL`: The protocol used to communicate with the Nexus Repository Manager.
- `NEXUS_URL`: The URL of the Nexus Repository Manager.
- `NEXUS_REPOSITORY`: The name of the repository to upload artifacts to.
- `NEXUS_REPO_ID`: The ID of the repository in Nexus.
- `NEXUS_CREDENTIAL_ID`: The ID of the credentials to use to authenticate with the Nexus Repository Manager.
- `ARTVERSION`: The version of the artifact to upload to the Nexus Repository Manager.

## Instructions

To use this pipeline, follow these steps:

1. Create a new pipeline job in Jenkins.

2. Copy the contents of this Jenkinsfile into the pipeline script field.

3. Set up the required environment variables for your Jenkins server.

4. Save the job and run the pipeline.

## Conclusion

This Jenkinsfile provides a template for building, testing, and deploying a Java web application using Jenkins, Maven, SonarQube, and Nexus Repository Manager. You can customize this pipeline to suit your specific needs, such as adding additional stages, using different tools, or integrating with other systems.
