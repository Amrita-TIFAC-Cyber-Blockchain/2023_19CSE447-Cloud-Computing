# 19CSE447 - Cloud Computing ![](https://img.shields.io/badge/-Live-brightgreen)
![](https://img.shields.io/badge/Batch-20EEE-lightgreen) ![](https://img.shields.io/badge/Batch-20ELC-lightgreen) ![](https://img.shields.io/badge/Batch-20CCE-lightgreen) ![](https://img.shields.io/badge/Batch-20ECE-lightgreen) ![](https://img.shields.io/badge/UG-blue) ![](https://img.shields.io/badge/Subject-Cloud-blue) ![](https://img.shields.io/badge/Subject-Elective-purple)  <br/>

## Practice Exercise 2 - Simple Flask Application

#### Create a directory like this

```
project-directory/
│
├── app.py
├── Dockerfile
└── requirements.txt (if needed)
```

#### Content for app.py

```
# app.py

from flask import Flask

app = Flask(__name__)

@app.route('/')
def home():
    return "Hello, this is the home route!"

@app.route('/info')
def info():
    return "This is some basic information."

if __name__ == '__main__':
    app.run(debug=True, host='0.0.0.0')
```

#### Content for Dockerfile

```
# Dockerfile

# Use the official Python image
FROM python:3.8

# Set the working directory in the container
WORKDIR /app

# Copy the requirements file and install dependencies (if you have any)
# COPY requirements.txt requirements.txt
# RUN pip install -r requirements.txt

# Copy the current directory contents into the container at /app
COPY . /app

# Install Flask
RUN pip install Flask

# Specify the command to run on container start
CMD ["python", "app.py"]

# Expose the port the app runs on
EXPOSE 5000
```

#### Build the Docker

```
docker build -t my-flask-app .
```

#### Run the Docker 

```
docker run -p 5000:5000 my-flask-app
```

#### Test the Application
- Home route: [http://localhost:5000/](http://localhost:5000/)
- Information route: [http://localhost:5000/info](http://localhost:5000/info)
