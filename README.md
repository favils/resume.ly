![CI/CD](https://github.com/software-students-fall2024/5-final-five/actions/workflows/web-app.yml/badge.svg)

# **📄 resume.ly**

## Description

This project is a software engineering exercise designed to demonstrate the integration of multiple subsystems, database management, containerization, deployment, and continuous integration/continuous deployment (CI/CD) practices. The project consists of a web application built with Python and a MongoDB database, orchestrated using Docker and deployed with GitHub Actions and Render.

### Features

- Subsystems: The project contains two primary subsystems:

    - A MongoDB database for storing user data and generated resumes.

    - A Python-based web application that serves as the interface for users to build, store, and access resumes.

- Dockerization: Each subsystem is containerized with its own Dockerfile, and the images are hosted on Docker Hub.

- CI/CD: Each subsystem is integrated with GitHub Actions for continuous integration and deployment. The CI/CD pipelines:

- Trigger on code changes (via push or pull request to the main or master branch).

- Build and test each subsystem.

- Deliver the Docker images to Docker Hub.

- Deploy the subsystems that are designed to run online to Render.

- Testing: The codebase contains unit tests with at least 80% test coverage for both subsystems.

<img src="public/login.png" alt="alt text" width="350"/>
<img src="public/gen.png" alt="alt text" width="350"/>

## Docker Image

You can access the Docker image for **resume.ly** on Docker Hub:

[**resume.ly Docker Image**](https://hub.docker.com/r/fav2019/flask-app)

## Try it out yourself
[Live Link](https://resume-generator-bxf0.onrender.com/login) 

## Run the App

### Environment Setup

Before running the app, ensure your `.env` file in the `web_app` directory contains the following MongoDB URI configuration:

```
MONGO_URI=mongodb+srv://user:pass@cluster0.5hb4r.mongodb.net/?retryWrites=true&w=majority&appName=Cluster0
```

Start by building:

```
docker-compose up --build
```

If you've already built previously, you may compose the containers like so:

```
docker-compose up
```

Once that is completed, you can access the site [HERE](http://localhost:8080/)


## Test Coverage

<img src="coverage.png" alt="coverage" width="300"/>
