---

# AWS Cloud – My Learning Journey

This repository contains my notes and understanding of **AWS Cloud Computing**.

---

# Day 14 Notes

# AWS End-to-End Continuous Integration

---

## AWS CodeBuild

**AWS CodeBuild** is a fully managed **Continuous Integration (CI)** service that compiles source code, runs automated tests, and produces software packages (artifacts) that are ready for deployment.

---

## How AWS CodeBuild Works

1. Developer pushes code (CodeCommit / GitHub / S3)
2. CodeBuild pulls the source code
3. Executes build commands from a `buildspec.yml` file
4. Runs automated tests
5. Generates output artifacts
6. Sends artifacts to:

   * Amazon S3
   * CodePipeline
   * CodeDeploy

---

## CodeBuild in CI/CD Flow

Developer → CodeCommit → CodePipeline → CodeBuild → CodeDeploy → Application

CodeBuild handles the **CI (Build + Test)** part of the pipeline.

---

# buildspec.yml

```yaml
version: 0.2

env:
  parameter-store:
    DOCKER_REGISTRY_USERNAME: /myapp/docker-credentials/username
    DOCKER_REGISTRY_PASSWORD: /myapp/docker-credentials/password

phases:
  install:
    runtime-versions:
      python: 3.11

  build:
    commands:
      - cd day-14/simple-python-app

      # Docker Hub login
      - echo "$DOCKER_REGISTRY_PASSWORD" | docker login -u "$DOCKER_REGISTRY_USERNAME" --password-stdin

      # Build Docker image
      - docker build -t "$DOCKER_REGISTRY_USERNAME/sample-python-app:latest" .

      # Push image to Docker Hub
      - docker push "$DOCKER_REGISTRY_USERNAME/sample-python-app:latest"

artifacts:
  files:
    - '**/*'
```

---

## Screenshots

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/39b3cd14d98b072dd9000285d0e99bbd8f699280/Day14%20%3A%20%20AWS%20END%20TO%20END%20Continous%20Integration/Day14%2001.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/39b3cd14d98b072dd9000285d0e99bbd8f699280/Day14%20%3A%20%20AWS%20END%20TO%20END%20Continous%20Integration/Day14%2002.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/39b3cd14d98b072dd9000285d0e99bbd8f699280/Day14%20%3A%20%20AWS%20END%20TO%20END%20Continous%20Integration/Day14%2003.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/39b3cd14d98b072dd9000285d0e99bbd8f699280/Day14%20%3A%20%20AWS%20END%20TO%20END%20Continous%20Integration/Day14%2004.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/39b3cd14d98b072dd9000285d0e99bbd8f699280/Day14%20%3A%20%20AWS%20END%20TO%20END%20Continous%20Integration/Day14%2005.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/39b3cd14d98b072dd9000285d0e99bbd8f699280/Day14%20%3A%20%20AWS%20END%20TO%20END%20Continous%20Integration/Day14%2006.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/39b3cd14d98b072dd9000285d0e99bbd8f699280/Day14%20%3A%20%20AWS%20END%20TO%20END%20Continous%20Integration/Day14%2007.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/39b3cd14d98b072dd9000285d0e99bbd8f699280/Day14%20%3A%20%20AWS%20END%20TO%20END%20Continous%20Integration/Day14%2008.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/39b3cd14d98b072dd9000285d0e99bbd8f699280/Day14%20%3A%20%20AWS%20END%20TO%20END%20Continous%20Integration/Day14%2009.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/39b3cd14d98b072dd9000285d0e99bbd8f699280/Day14%20%3A%20%20AWS%20END%20TO%20END%20Continous%20Integration/Day14%2010.png)

![image](https://github.com/adhikarilaxman/AWS-Journey/blob/39b3cd14d98b072dd9000285d0e99bbd8f699280/Day14%20%3A%20%20AWS%20END%20TO%20END%20Continous%20Integration/Day14%2011.png)

![image[]()](https://github.com/adhikarilaxman/AWS-Journey/blob/39b3cd14d98b072dd9000285d0e99bbd8f699280/Day14%20%3A%20%20AWS%20END%20TO%20END%20Continous%20Integration/Day14%2012.png)

---
