# GitHub Issue AI Assistant

GitHub Issue AI Assistant is an AI-powered application that analyzes GitHub issues
and generates structured JSON insights including issue summary, issue type,
priority score, suggested labels, and potential impact.

## What This Project Does

The application performs the following steps:
1. Accepts a GitHub issue URL from the user
2. Fetches the issue title, body, and comments using the GitHub API
3. Analyzes the issue using an AI model
4. Enforces a strict JSON output format
5. Displays the result in a simple web interface
6. Allows the user to download the JSON output

## System Requirements

- Python  3.11
- Git

## How to Execute the Project (Step-by-Step)

Follow the steps below exactly in the given order.

### Step 1: Clone the Repository

git clone https://github.com/kavyaboompur/github-issue-ai-assistant.git
cd github-issue-ai-assistant

### Step 2: Create a Virtual Environment

python -m venv venv
### Step 3: Activate the Virtual Environment

venv\Scripts\activate
Ensure `(venv)` appears in the terminal before continuing.
### Step 4: Install Dependencies

pip install -r requirements.txt

### Step 5: Start the Backend Server

python -m uvicorn backend.main:app --port 8000 --reload

Keep this terminal window open.

---

### Step 6: Start the Frontend Application

Open a new terminal window.
cd github-issue-ai-assistant 
venv\Scripts\activate
streamlit run frontend/app.py
Common Errors and Fixes

Python not recognized: Ensure Python is installed and added to PATH

Missing modules: Activate the virtual environment and reinstall dependencies

Frontend error: Ensure the backend is running before starting the frontend

### results is being provide in google drive link = 
### incase  i have captured screenshots how to execute step by step here is google drive link = https://drive.google.com/file/d/1p0RtVNFa7DPiTowxK4ZMbQQsdTN5I5PQ/view?usp=sharing

