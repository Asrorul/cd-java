# GitHub Actions Workflow: Maven Package Publishing

This workflow automates the process of building and publishing Maven packages to GitHub Packages when a new release is created.

## Workflow Overview

The workflow is triggered when a new release is created in the repository and performs the following steps:

1. **Environment Setup**
   - Runs on Ubuntu latest
   - Uses JDK 11 (Temurin distribution)
   - Configures necessary permissions for reading contents and writing packages

2. **Build Process**
   - Checks out the repository code
   - Sets up Java development environment
   - Configures Maven settings for GitHub Packages
   - Builds the project using Maven
   - Publishes the package to GitHub Packages

## Prerequisites

- A GitHub repository with Java/Maven project
- `pom.xml` file properly configured with distribution management
- Appropriate permissions to create releases and publish packages

## Usage

1. Create a new release in your GitHub repository
2. The workflow will automatically:
   - Build your Maven package
   - Publish it to GitHub Packages

## Environment Variables

- `GITHUB_TOKEN`: Automatically provided by GitHub Actions for authentication
- `GITHUB_WORKSPACE`: The path where your repository is checked out

## Additional Information

For more detailed information about Java setup and advanced usage, refer to:
https://github.com/actions/setup-java/blob/main/docs/advanced-usage.md#apache-maven-with-a-settings-path
