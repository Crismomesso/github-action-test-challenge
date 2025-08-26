# github-action-test-challenge
# Challenge: Full Stack Deployment with AWS

This project is a challenge to deploy a full stack application using modern CI/CD practices and AWS services.

## Overview

- **Frontend:** Angular application deployed to AWS S3 using GitHub Actions and `ng deploy`.
- **Backend:** .NET (or Java) backend containerized, pushed to Amazon ECR, and deployed to AWS ECS via GitHub Actions.

## Frontend Deployment

- Uses Angular CLI and `ngx-deploy-s3` for direct deployment to S3.
- GitHub Actions workflow (`frontend-angular.yml`) automates:
  - Linting, testing, and building the Angular app.
  - Deploying to the specified S3 bucket on pushes to `main`.

## Backend Deployment

- Backend is built as a Docker image.
- GitHub Actions workflow (`backend-dotnet.yml`) automates:
  - Building and pushing the Docker image to Amazon ECR.
  - Updating the ECS task definition and deploying to ECS.

## Requirements

- AWS account with S3, ECR, and ECS set up.
- GitHub repository with the provided workflows.
- AWS credentials stored as GitHub secrets.

## How to Use

1. Configure your S3 bucket and update the Angular deploy options.
2. Set up ECR, ECS cluster, and task definition for the backend.
3. Add AWS credentials as GitHub secrets.
4. Push to `main` to trigger the CI/CD pipelines.

---

This repository demonstrates a complete CI/CD pipeline for a full stack application as part of a technical challenge.