## 🐙 GitHub Issue AI Assistant

GitHub Issue AI Assistant is an AI-powered application that analyzes GitHub issues and generates structured, actionable insights in JSON format.
It helps developers and teams quickly understand issue severity, type, priority, and potential impact using AI.

## 🚀 What This Project Does

This application performs the following steps:

Accepts a GitHub issue URL and issue number via a Streamlit web interface

Fetches issue title, description, and comments using the GitHub REST API

Processes the issue data using an LLM-based AI model (Hugging Face Transformers)

Applies a strict structured prompt to ensure valid JSON output

Serves AI analysis through a FastAPI backend

Displays results in a clean, readable UI

Allows users to download the generated JSON output

## 🧠 Why This Project Matters

Saves developer time by summarizing complex GitHub issues

Converts unstructured issue discussions into structured data

Demonstrates real-world LLM integration, API usage, and backend–frontend coordination

Mimics how AI tools are built in modern engineering teams

## 🛠 Tech Stack

Backend: FastAPI, Python 3.11

Frontend: Streamlit

AI / LLM: Hugging Face Transformers

APIs: GitHub REST API

Others: Requests, Uvicorn

## 📁 Project Structure

After extracting the ZIP files, the directory should look like this:

github-issue-ai-assistant/

│
├── backend/

│   ├── main.py        # FastAPI entry point

│   ├── llm.py         # AI / LLM logic

│   ├── github.py      # GitHub API integration

│   ├── schemas.py     # Request & response schemas

│   ├── config.py      # Configuration

│   └── __init__.py
│

├── frontend/
│   └── app.py         # Streamlit UI
│

├── requirements.txt

└── README.md


## Important:
If ZIP files are not extracted correctly, backend or frontend commands will fail due to missing paths.

## Important Fixes Implemented

Corrected all import paths in main.py to resolve repeated ModuleNotFoundError

Aligned execution commands with the actual extracted folder structure

Ensured backend runs from the project root, not inside subfolders

System Requirements
Required Software

Python 3.11 (Recommended strictly : 3.11.9)

Git

Extracted project source files (ZIP)

## How to Run the Project (Step-by-Step)

Follow these steps in order.

## Step 1: Clone the Repository
git clone https://github.com/kavyaboompur/github-issue-ai-assistant.git

cd github-issue-ai-assistant

## Step 2: Create a Virtual Environment
python -m venv venv

## Step 3: Activate the Virtual Environment

venv\Scripts\activate

Ensure (venv) appears in the terminal.

## Step 4: Install Dependencies
pip install -r requirements.txt

Step 5: Start the Backend Server

Check backend folder path first:

cd backend

dir

Run the backend based on extracted structure:

python -m uvicorn backend.main:app --reload --port 8000

If ZIP extraction created nested folders, use:

python -m uvicorn backend.backend.main:app --reload --port 8000

Note:if found error then use crct path

Backend API will be available at:

http://localhost:8000/analyze

Keep this terminal open.

## Common Backend Error & Fix
Error:
ModuleNotFoundError: No module named 'backend'

Root Cause:
Python could not resolve module paths because execution was done from the wrong directory

Solution:
Identified correct folder hierarchy

Updated imports such as:
from backend.backend.llm import IssueAnalyzer,
from backend.llm import IssueAnalyzer
OR

from llm import IssueAnalyzer

Executed the server from the project root

Step 6: Start the Frontend (New Terminal)
cd github-issue-ai-assistant
venv\Scripts\activate

If Streamlit is missing:

pip install streamlit

Run the frontend:

streamlit run frontend/app.py
(Adjust path if folders differ due to ZIP extraction.)

## How to Use the Application

Click Start

Enter GitHub repository URL

Enter issue number

Click Analyze Issue

Wait for AI processing

View readable summary

Click View Result for JSON

Download JSON output if needed

## Example Results & Screenshots

Screenshots and example outputs are available here:
🔗 https://drive.google.com/file/d/1an2VZ27TGhHyTDghLzRciyoy7-6uZeSl/view

Included Screens:

Application home page

Issue input screen

Processing state

AI-generated summary

Priority score & labels

Full JSON output

Backend & frontend running successfully

## Step-by-Step Execution Screenshots

Visual execution guide available here:
🔗 https://drive.google.com/file/d/1p0RtVNFa7DPiTowxK4ZMbQQsdTN5I5PQ/view
