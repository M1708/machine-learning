---
title: "Docker-Readme"
author: "Meenu"
date: "29/04/2021"
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

# Project Title

Docker for ML

## Description

This project will help you understand  how to train machine learning models using docker. It will help you serialize models within the image for easy retrieval and will allow you to perform batch inference using docker container. Perform online inference using RESTful api and Flask.

## Getting Started

### Installing

* Python 3
* Docker
* Flask


### Files and Folders

* jupyter-custom-docker 
  * Dockerfile - contains all the requirements that would build up a custom docker image
* model-training
  * For batch inference
* online-reference
  * For real-time inference

### Executing program

* sudo docker ps     ##check docker processes running
* sudo docker images     ##docker images on our system
* sudo docker pull <image name>      ##pull an image
* sudo docker run --rm -ti python3.6 python      ##fireup python3.6 interpreter
* sudo docker run --rm -p 8080:8080 jupyter/scipy-notebook      ##run jupyter scipy notebook
* sudo docker build -t <docker image name>      ##build docker image
* sudo docker run <docker image name> python3 inference.py       ##for batch inference
* sudo docker run -it -p 5000:5000 docker.api python3 api.py       ##run docker container in interactive mode
* curl -i -H "Content-Type: application/json" -X POST -d '{"CRIM": 15.02, "ZN": 0.0, "INDUS": 18.1, "CHAS": 0.0, "NOX": 0.614, "RM": 5.3, "AGE": 97.3, "DIS": 2.1, "RAD": 24.0, "TAX": 666.0, "PTRATIO": 20.2, "B": 349.48, "LSTAT": 24.9}' 127.0.0.1:5000/predict       ##issue the post request, pass each field value and obtain the response


## Acknowledgments
* [Coursera](https://coursera.org)