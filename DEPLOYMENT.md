# Deployment of PySpark Pipeline

## 1. Deployment Using GitHub Actions

The PySpark pipeline is deployed using **GitHub Actions** to ensure automated, repeatable, and consistent deployments.

### Deployment Steps
- Developer pushes code to the GitHub repository.
- GitHub Actions workflow is triggered on `push` or `pull_request`.
- CI pipeline runs:
  - Unit tests for PySpark functions
  - Basic validation checks
- On successful validation:
  - Application code (or Docker image) is built.
  - Artifacts are prepared for execution using `spark-submit`.

This approach eliminates manual deployment and ensures only tested code is deployed.
