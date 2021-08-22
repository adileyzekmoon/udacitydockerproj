[![CircleCI](https://circleci.com/gh/adileyzekmoon/udacitydockerproj/tree/main.svg?style=svg)](https://circleci.com/gh/adileyzekmoon/udacitydockerproj/tree/main)

## Project Overview

In this project, you will apply the skills you have acquired in this course to operationalize a Machine Learning Microservice API. 

You are given a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project tests your ability to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

### Project Tasks

Your project goal is to operationalize this working, machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications. In this project you will:
* Test your project code using linting
* Complete a Dockerfile to containerize this application
* Deploy your containerized application using Docker and make a prediction
* Improve the log statements in the source code for this application
* Configure Kubernetes and create a Kubernetes cluster
* Deploy a container using Kubernetes and make a prediction
* Upload a complete Github repo with CircleCI to indicate that your code has been tested

You can find a detailed [project rubric, here](https://review.udacity.com/#!/rubrics/2576/view).

**The final implementation of the project will showcase your abilities to operationalize production microservices.**

---

## Setup the Environment

* Create a virtualenv and activate it
* Run `make install` to install the necessary dependencies
    Required depenencies:
    1. hadolint
    2. pylint


### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
    Required depenencies:
    1. minikube
    2. kubectl 
* Create Flask app in Container
* Run via kubectl

### Relevant enhanced files for project

* output_txt_files
    1. docker_out.txt: console output for on Docker when app.py is run on Docker
    2. kubernetes.txt: console output for on Kubernetes cluster when app.py is run on Kubernetes
* Dockerfile: configuration file for running docker setup and commands
* Makefile: configuration file for make commands
* requirements.txt: required python dependencies, includes pylint for Makefile
* run_docker.sh: Shell script to run Flask image on Docker
* run_kubernetes.sh: Shell script to run Flask image on Kubernetes cluster
* upload_docker.sh: Shell script to upload Docker image to remote repository 
