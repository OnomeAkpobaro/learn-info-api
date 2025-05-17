*INFO API*
A simple public API that returns basic personal information in JSON format, including email address, current datetime, and GitHub URL.
Features

Returns personal information in JSON format
Dynamically generates current UTC datetime in ISO 8601 format
CORS enabled for cross-origin requests
Fast response time (< 500ms)
Simple health check endpoint

API Specification
Endpoint

GET https://learn-info-api.onrender.com/

Response Format
json{
  "email": "your-email@example.com",
  "current_datetime": "2025-05-16T09:30:00Z", 
  "github_url": "https://github.com/yourusername/learn-info-api"
}
Tech Stack

Framework: FastAPI
Language: Python 3.8+
Web Server: Uvicorn
Deployment: Render

Local Development Setup
Prerequisites

Python 3.8 or higher
pip (Python package manager)

Installation

Clone the repository

bashgit clone https://github.com/onomeakpobaro/learn-info-api.git
cd info-api

Create and activate a virtual environment (optional but recommended)

bashpython -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

Install the dependencies

bashpip install -r requirements.txt

Update your personal information in main.py

python# In the get_info function, update:
"email": "your-email@example.com"  # Replace with your actual email
"github_url": "https://github.com/yourusername/learn-info-api"  # Replace with your actual GitHub URL

Run the server locally

bashpython main.py

Access the API at http://localhost:8000 and the API documentation at http://localhost:8000/docs

Deployment
Option 1: Railway

Create an account on Railway
Create a new project from your GitHub repository
Set up the deployment settings:

Build Command: pip install -r requirements.txt
Start Command: uvicorn main:app --host 0.0.0.0 --port $PORT


Deploy your application

Option 2: Render

Create an account on Render
Create a new Web Service from your GitHub repository
Set up the deployment settings:

Build Command: pip install -r requirements.txt
Start Command: uvicorn main:app --host 0.0.0.0 --port $PORT


Deploy your application

Option 3: Heroku

Create an account on Heroku
Install the Heroku CLI and login
Create a new app and set it up for deployment

bashheroku create your-app-name
git push heroku main
Testing
To test the API, you can use tools like:

Your web browser (for GET requests)
cURL from the command line
API testing tools like Postman or Insomnia

Example cURL command:
bashcurl -X GET https://your-deployed-url.com/
API Documentation
FastAPI automatically generates API documentation. Once the server is running, you can access:

Swagger UI: https://your-deployed-url.com/docs
ReDoc: https://your-deployed-url.com/redoc

Related Resources

HNG Internship - Hire Python Developers

License
This project is licensed under the MIT License - see the LICENSE file for details.
