# Dockerize-Flask-App
A simple Flask application that says Hello COSC!

## Getting Started

To dockerize this Flask application, follow these steps:

1. Create a `Dockerfile` in the root directory
    add the below code 

    First we are fetching the image of python to execute or provide this environment  
    FROM python:3.10-slim

    creating the root directory  
    WORKDIR /app

    copy the existing file contents.  
    COPY requirements.txt .

    run the or install the dependencies  
    RUN pip install --no-cache-dir -r requirements.txt

    copy everything from the root directory to the workdir/app root directory  
    COPY . .

    give a port number later for port binding  
    EXPOSE 6009

    need to write the executing commands in the list. separted by comma.  
    CMD ["python", "app.py"]

2. Add a `.dockerignore` file to exclude unnecessary files

## Instructions

Create the necessary Docker configuration files to containerize this Flask application. 