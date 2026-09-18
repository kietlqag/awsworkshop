# AWS Workshop - Spring Boot Deployment

Hugo-based workshop documentation for deploying a Spring Boot application to AWS Elastic Beanstalk with Aurora Serverless MySQL and GitHub Actions CI/CD. The source pages live under `content/`, and the generated static site is stored in `docs/`.

## Project Summary

| Area | Implementation |
|---|---|
| Documentation engine | Hugo with the `hugo-theme-learn` theme |
| Workshop scope | Spring Boot deployment to AWS Elastic Beanstalk |
| Networking | Custom VPC and security group walkthrough |
| Database | Aurora Serverless MySQL setup, including Data API-oriented steps |
| Application hosting | Elastic Beanstalk deployment flow |
| CI/CD | GitHub Actions deployment guidance |
| Static output | Generated site in `docs/` for GitHub Pages-style hosting |
| Configuration | Hugo site settings in `config.toml` |
| Secrets | Real AWS and GitHub credentials must be kept outside the repository |

## Workshop Modules

1. Introduction and prerequisites
2. Environment preparation
3. Custom VPC setup
4. Security group setup
5. Aurora Serverless MySQL setup
6. Elastic Beanstalk deployment
7. Application testing
8. GitHub Actions CI/CD configuration
9. Resource cleanup

## Requirements

- AWS account with permissions for VPC, EC2/Elastic Beanstalk, RDS/Aurora, IAM, and related services
- GitHub account for CI/CD practice
- Basic Spring Boot and AWS knowledge
- Hugo, when editing or regenerating the documentation site

## Run Locally

```bash
hugo server
```

The local URL is usually:

```text
http://localhost:1313
```

## Build Static Site

```bash
hugo
```

The generated files are written to `docs/`.

## Security Notes

- Do not commit AWS access keys, secret access keys, session tokens, private keys, `.env` files, or GitHub tokens.
- Store CI/CD values in GitHub Actions Secrets.
- Use local AWS profiles or AWS-managed configuration for workshop execution.
- Run the cleanup module after testing to avoid unexpected AWS charges.
