+++
title = "Portfolio Build & Deployment"
showonlyimage = false
draft = false
image = "img/portfolio/project_1.jpg"
date = 2025-06-08
weight = 3
+++

In additon to highllighting specific projects, this portfolio website is also a live demonstration of my skills in DevOps, cloud automation, and reproducible publishing workflows. <!--more--> It is generated using [**Hugo**](https://gohugo.io/), a fast static site generator written in Go, and is designed to be fully version-controlled, reproducible, and automatically deployed via a cloud-native CI/CD pipeline.

---

### Project at a Glance

This site pipeline demonstrates:

- **Infrastructure-as-code and CI/CD** using AWS CodeBuild, IAM, and GitHub
- **Fully automated deployment** of a static site to a CDN-backed global endpoint
- **Content-driven engineering** using Hugo and modular markdown structures
- **Security-aware design** with scoped IAM roles and reproducible builds

---

### Pipeline Overview

#### 1. Local Development

- Content is authored in markdown using Hugo’s `content/` structure and organized by theme-defined sections (e.g., `about`, `portfolio`, `projects`)
- Theme customization is handled via the `creative-portfolio-mb` Hugo theme with parameters set in `config.toml`
- Pages are previewed locally using `hugo server` for rapid iteration

#### 2. Version Control & GitHub Integration

- The entire site (content, configuration, theme, assets) is tracked in Git and hosted in a GitHub repository
- Commits to the `main` branch represent production-ready changes

#### 3. Continuous Deployment via AWS CodeBuild

- A GitHub webhook triggers an AWS CodeBuild project whenever a push is made to `main`
- The build process is defined in a `buildspec.yml` file, which includes:
  - Installing Hugo
  - Building the static site with `hugo`
  - Deploying the site to an [Amazon S3](https://aws.amazon.com/s3/) bucket configured for static website hosting
  - Invalidating the [CloudFront](https://aws.amazon.com/cloudfront/) cache to ensure instant global propagation of updates

#### 4. Secure & Automated Delivery

- Deployment credentials are scoped via IAM to permit only S3 and CloudFront actions
- AWS CLI is optionally configured locally to allow manual `hugo deploy` overrides
- Assets are delivered over HTTPS via CloudFront with long-term caching policies defined in `config.toml`

---





