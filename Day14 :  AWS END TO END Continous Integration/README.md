---

# AWS Cloud – My Learning Journey

This repository contains my notes and understanding of **AWS Cloud Computing**.

---

## Day 14 Notes

# AWS End-to-End Continuous Integration

---

## AWS CodeBuild

**AWS CodeBuild** is a fully managed **Continuous Integration (CI)** service that compiles source code, runs tests, and produces software packages (artifacts) that are ready for deployment.

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

CodeBuild handles the **CI part (Build + Test)** of the pipeline.

---

## Screenshots

![image]()

![image]()

![image]()

![image]()

![image]()

![image]()

![image]()

![image]()

![image]()

![image]()

![image]()

![image]()

![image]()

![image]()

![image]()

![image]()
