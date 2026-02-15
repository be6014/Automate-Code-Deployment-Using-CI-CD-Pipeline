# DevOps Internship Task 1 – CI/CD Pipeline (GitHub Actions)

## Objective
Automate build and deployment of a Node.js web app using GitHub Actions and Docker.

## Tools
- GitHub
- GitHub Actions
- Node.js
- Docker / DockerHub

## Project Structure
```
.
├── app/
│   ├── index.js
│   └── package.json
├── Dockerfile
└── .github/workflows/main.yml
```

## CI/CD Workflow
1. Trigger on push to main
2. Install dependencies
3. Run tests
4. Build Docker image
5. Push image to DockerHub

## Setup Steps
1. Create GitHub repo and upload files
2. Add secrets in GitHub → Settings → Secrets:
   - DOCKERHUB_USERNAME
   - DOCKERHUB_TOKEN
3. Push to main branch
4. Check Actions tab for pipeline run

## Run Locally
```
docker build -t nodejs-demo .
docker run -p 3000:3000 nodejs-demo
```

## Screenshots
See `/screenshots` folder.

## Interview Q&A (Short)
- CI/CD: Continuous Integration & Deployment automation
- GitHub Actions: Workflow automation via YAML
- Runner: VM executing jobs
- Jobs vs Steps: Job = group, Step = command
- Secrets: Encrypted repo settings
- Local test: act or Docker build
