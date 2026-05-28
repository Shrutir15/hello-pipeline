#  Automated Container Build Pipeline

## Objective
Grasp the fundamentals of containerisation and automated workflows by packaging a simple application into a container and setting up an automated pipeline that builds and stores the container image every time code is committed.

---

## Tech Stack
- **Language:** Python 3.9
- **Framework:** Flask
- **Containerization:** Docker
- **CI/CD:** GitHub Actions
- **Image Registry:** Docker Hub

---

## Project Structure

hello-pipeline/
├── app.py                            # Hello World Flask web application
├── Dockerfile                        # Container configuration
├── requirements.txt                  # Python dependencies
└── .github/
    └── workflows/
        └── docker-build.yml          # GitHub Actions CI/CD workflow

---

## Application
A simple Hello World web application built with Python and Flask that returns:

Hello World! Automated Container Pipeline is working!

---

## Dockerfile
The Dockerfile:
- Uses official Python 3.9 slim base image
- Sets working directory to /app
- Installs all dependencies from requirements.txt
- Exposes port 5000
- Runs the Flask application

---

## GitHub Actions Workflow
The workflow is triggered automatically on every push to the main branch and performs the following steps:
1. Checks out the code from the repository
2. Logs in to Docker Hub using GitHub Secrets
3. Builds the Docker image from the Dockerfile
4. Pushes the image to Docker Hub with the latest tag

---

## How to Run Locally
Make sure Docker is installed and running, then execute:

docker pull ss22csb0a08/hello-pipeline
docker run -p 5000:5000 ss22csb0a08/hello-pipeline

Then open your browser and go to:

http://localhost:5000

---

## CI/CD Pipeline Results
- Every push to main branch automatically triggers the pipeline
- Docker image is built and pushed to Docker Hub
- Pipeline completes successfully in under 30 seconds

---

## Deliverables

### GitHub Repository
https://github.com/Shrutir15/hello-pipeline

### Successful GitHub Actions Run
https://github.com/Shrutir15/hello-pipeline/actions

### Docker Hub Image
https://hub.docker.com/r/ss22csb0a08/hello-pipeline

---

## Author
- **GitHub:** https://github.com/Shrutir15
- **Docker Hub:** https://hub.docker.com/u/ss22csb0a08