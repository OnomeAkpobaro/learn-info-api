*INFO API*


A simple public API that returns basic personal information in JSON format, including email address, current datetime, and GitHub URL.


*Features*

Returns personal information in JSON format
Dynamically generates current UTC datetime in ISO 8601 format
CORS enabled for cross-origin requests
Fast response time (< 500ms)
Simple health check endpoint



*Endpoint*

GET https://info-api-9daa.onrender.com/

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

bash git clone https://github.com/onomeakpobaro/learn-info-api.git
cd info-api

Create and activate a virtual environment (optional but recommended)

bash python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

Install the dependencies

bash pip install -r requirements.txt

Update your personal information in main.py


"email": "your-email@example.com"  # Replace with your actual email
"github_url": "https://github.com/yourusername/learn-info-api"  # Replace with your actual GitHub URL

Run the server locally

bash python main.py

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






License
This project is licensed under the MIT License - see the LICENSE file for details.
