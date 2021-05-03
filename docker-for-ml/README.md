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

* sudo docker ps ##check docker processes running
* sudo docker images ##docker images on our system
* sudo docker pull <image name> ##pull an image
* sudo docker run --rm -ti python3.6 python ##fireup python3.6 interpreter
* sudo docker run --rm -p 8080:8080 jupyter/scipy-notebook ##run jupyter scipy notebook
* sudo docker build -t <docker image name> ##build docker image
* sudo docker run <docker image name> python3 inference.py ##for batch inference
* sudo docker run -it -p 5000:5000 docker.api python3 api.py ##run docker container in interactive mode
* curl -i -H "Content-Type: application/json" -X POST -d '{"CRIM": 15.02, "ZN": 0.0, "INDUS": 18.1, "CHAS": 0.0, "NOX": 0.614, "RM": 5.3, "AGE": 97.3, "DIS": 2.1, "RAD": 24.0, "TAX": 666.0, "PTRATIO": 20.2, "B": 349.48, "LSTAT": 24.9}' 127.0.0.1:5000/predict ##issue the post request, pass each field value and obtain the response

```
code blocks for commands
```

## Help

Any advise for common problems or issues.
```
command to run if program contains helper info
```

## Authors

Contributors names and contact info

ex. Dominique Pizzie  
ex. [@DomPizzie](https://twitter.com/dompizzie)

## Version History

* 0.2
    * Various bug fixes and optimizations
    * See [commit change]() or See [release history]()
* 0.1
    * Initial Release

## License

This project is licensed under the [NAME HERE] License - see the LICENSE.md file for details

## Acknowledgments

Inspiration, code snippets, etc.
* [awesome-readme](https://github.com/matiassingers/awesome-readme)
* [PurpleBooth](https://gist.github.com/PurpleBooth/109311bb0361f32d87a2)
* [dbader](https://github.com/dbader/readme-template)
* [zenorocha](https://gist.github.com/zenorocha/4526327)
* [fvcproductions](https://gist.github.com/fvcproductions/1bfc2d4aecb01a834b46)