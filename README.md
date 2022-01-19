# General
An simple example on how to deploy machine learning model using docker and fastapi.

## To run:
### Locally
I recommend using docker below, but also works like this:
`poetry install` # to install to python env
`cd TO/PATH`
`uvicorn main:app --reload`

### Using Docker
cd to the folder: `cd PATH/TO/api-tita`
run docker: `docker-compose up --build`

### Find Solution at
recommended: go in browser to http://localhost/docs 

## For dev purposes
tests: `python -m main`
run server: `uvicorn main:app --reload`

## Troubleshoot
find IP: `docker ps`

## Files
'main.py' holds the API-related code. We put all in one file to make project simpler.
'test.py' has one test case to validate classifier is roughly working.
'Dockerfile' configures the server and installs dependencies. I used the Uvicorn/FastApi
'docker-compose.yml' not really needed. Simplifies execution on your side. I put restart: always incase you test edge cases (I did not handle them). 
'make_model.py' builds and selects a model. I did not validate them much since this is more of an API tutorial.

## Data From
Kaggle: https://www.kaggle.com/c/titanic-dataset/data

## CI/CD with GitHub actions 
I also implemented to CI/CD pipeline which allows followings tasks when push or pull request on master branch
1 - set up python
2 - Install dependencies with requirements.txt
3 - Lint with fake8
4 - Unittest python script
5 - and Build and Push docker Image on dockerhub
=======
## CI/CD with GitHub actions
I also implemented to CI/CD pipeline which allows followings tasks when push or pull request on master branch 1 - set up python 2 - Install dependencies with requirements.txt 3 - Lint with fake8 4 - Unittest python script 5 - and Build and Push docker Image on dockerhub

