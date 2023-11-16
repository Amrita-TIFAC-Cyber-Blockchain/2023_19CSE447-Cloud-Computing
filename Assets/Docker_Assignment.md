# 19CSE447 - Cloud Computing ![](https://img.shields.io/badge/-Live-brightgreen)
![](https://img.shields.io/badge/Batch-20EEE-lightgreen) ![](https://img.shields.io/badge/Batch-20ELC-lightgreen) ![](https://img.shields.io/badge/Batch-20CCE-lightgreen) ![](https://img.shields.io/badge/Batch-20ECE-lightgreen) ![](https://img.shields.io/badge/UG-blue) ![](https://img.shields.io/badge/Subject-Cloud-blue) ![](https://img.shields.io/badge/Subject-Elective-purple)  <br/>

## Assignment: Create a Docker Image for a Database Connector

###  Objective:
Build a Docker image for a database connector application. The application connects to a database using a specific programming language and requires the installation of certain packages. Set environment variables for database connection details and expose the application on a specific IP address and port.

### Requirements:
 - Choose a base image appropriate for the chosen programming language (e.g., Python, Node.js, Ruby).
 - Install the necessary packages for connecting to a database. Choose a simple database connector library compatible with your chosen language (e.g., psycopg2 for Python, mysql2 for Node.js, pg for Ruby).
 - Set environment variables for the following database connection details:
   - Database host
   - Database port
   - Database username
   - Database password
   - Database name
 - Expose the application on a specific IP address and port (e.g., IP: 0.0.0.0, Port: 8080).
 - Create a sample application code that uses the installed database connector library to connect to a database (you can use dummy values for the connection).

### Tips:
 - Use an official base image related to the chosen programming language.
 - Clearly document each step in the Dockerfile using comments.
 - Make sure to expose the correct port for your application.
 - Test the Docker image locally to ensure the database connector application is running.

### Submission:
Provide the following in your submission:
 - The Dockerfile used to build the Docker image.
 - The source code of the sample application demonstrating the database connection.
 - Link to Image in Docker Hub.

Deadline: 20th Nov, 2023
