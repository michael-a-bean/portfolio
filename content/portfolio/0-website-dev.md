+++
title = "Portfolio Build & Deployment"
showonlyimage = false
draft = false
image = "img/portfolio/project_1.jpg"
date = 2025-06-08
weight = 3
+++

I built this portfolio with [Hugo](https://gohugo.io/) and automated its deployment with AWS CodeBuild, Amazon S3, and CloudFront. <!--more--> The site’s content, configuration, theme, and assets are tracked in Git. A push to `main` triggers the build and deployment process.

---

### Project at a Glance

The site uses:

- Hugo content files and templates
- Git and GitHub for version control
- AWS CodeBuild for deployment to Amazon S3
- CloudFront for content delivery and IAM for deployment permissions

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
  - Invalidating the [CloudFront](https://aws.amazon.com/cloudfront/) cache to refresh cached content after deployment

#### 4. Secure & Automated Delivery

- Deployment permissions are managed through IAM
- AWS CLI is optionally configured locally to allow manual `hugo deploy` overrides
- Assets are delivered over HTTPS via CloudFront with long-term caching policies defined in `config.toml`

---





