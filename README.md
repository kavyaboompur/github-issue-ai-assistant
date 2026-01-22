# GitHub Issue AI Assistant

GitHub Issue AI Assistant is an AI-powered application that analyzes GitHub issues
and generates structured JSON insights including issue summary, issue type,
priority score, suggested labels, and potential impact.

## What This Project Does

The application performs the following steps:

1.Accepts a GitHub issue URL from the user through a Streamlit web interface

2.Fetches the issue title, body, and comments using the GitHub REST API via the requests library

3.Processes the collected issue data using an LLM-based AI model implemented with Hugging Face Transformers

4.Applies a structured prompt to ensure the AI returns output in a strict JSON schema

5.Serves the AI analysis through a FastAPI backend endpoint

6.Displays the structured results in the Streamlit frontend in a readable format

7.Allows the user to download the generated JSON output for further use

## System Requirements

You may download the ZIP file and follow the step-by-step execution screenshots available at the link below, or proceed with the instructions provided in this README:

https://drive.google.com/file/d/1p0RtVNFa7DPiTowxK4ZMbQQsdTN5I5PQ/view?usp=sharing

## Important Note About Project Files (ZIP Format)

The backend and frontend source code are provided in ZIP format in this repository.

Before executing the project, please follow the steps below carefully:

1. Download the repository as a ZIP file **or** clone the repository using Git.

2. Locate the files `backend.zip` and `frontend.zip` in the project root.

3. Extract `backend.zip` to create a folder named `backend`.

4. Extract `frontend.zip` to create a folder named `frontend`.

5. Ensure the final folder structure looks like this:

## Project Structure

After extracting the ZIP files, ensure the project directory is structured as shown below:


github-issue-ai-assistant/
├── backend/
│ ├── main.py # FastAPI entry point
│ ├── llm.py # AI / LLM processing logic
│ ├── github.py # GitHub API integration
│ ├── schemas.py # Request and response schemas
│ ├── config.py # Configuration and constants
│ └── init.py
│
├── frontend/
│ └── app.py # Streamlit user interface
│
├── requirements.txt # Project dependencies
└── README.md # Project documentation


The `backend` directory contains all server-side logic, including GitHub data fetching, AI processing, and API endpoints.  

The `frontend` directory contains the Streamlit application used for user interaction and result display.

Make sure both the `backend` and `frontend` folders are present before running the execution commands.


6. After extraction, proceed with the execution steps described below.

If the ZIP files are not extracted correctly, commands such as starting the backend
or frontend will fail due to missing paths.

### Required Software

- **Python 3.11**
  - Recommended version: **Python 3.11.9**
  - This version is required to ensure compatibility with all project dependencies

- **Git**
  - Required to clone the repository

- **Source Files (ZIP Format)**
  - Project files are provided in ZIP format.
  - If any errors related to missing files occur, ensure the ZIP file is completely downloaded and extracted before running the project.

## How to Execute the Project (Step-by-Step)

Follow the steps below exactly in the given order.
Ensure you are in the correct project directory before running the commands below.  
All required software and dependencies must be installed before proceeding.


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

Note: The following command works the same in Windows Command Prompt, PowerShell, and most terminal environments, provided the virtual environment is activated.

python -m uvicorn backend.main:app --port 8000 --reload

Keep this terminal window open.

---

### Step 6: Start the Frontend Application

### Open a new terminal window.
cd github-issue-ai-assistant 

venv\Scripts\activate

streamlit run frontend/app.py
### Common Errors and Fixes

Python not recognized: Ensure Python is installed and added to PATH

Missing modules: Activate the virtual environment and reinstall dependencies

Frontend error: Ensure the backend is running before starting the frontend
### How to Use the Streamlit Frontend to Get Results

1.Click the Start button when the application loads

2.Copy and paste the GitHub repository URL

3.Enter the issue number

4.Click Analyze Issue

5.Wait until the analysis is completed

6.View the clean and readable analysis summary

7.Click View Result to see the JSON output

8.Optionally preview the GitHub issue

9.Download the JSON output using the Download JSON button

## Example Results and Screenshots

The example output results and application screenshots are available at the following
Google Drive link:https://drive.google.com/file/d/1an2VZ27TGhHyTDghLzRciyoy7-6uZeSl/view?usp=sharing
### Screenshot Descriptions

Screenshot (135).png – Home page of the GitHub Issue AI Assistant application.

Screenshot (136).png – Screen where the user enters the GitHub issue URL and issue number.

Screenshot (137).png – Example showing a GitHub issue URL entered for analysis.

Screenshot (138).png – Application processing the issue after clicking the Analyze button.

Screenshot (139).png – Display of the generated issue summary after analysis.

Screenshot (140).png – Output showing the issue type and priority score.

Screenshot (141).png – Suggested labels and potential impact generated by the AI.

Screenshot (142).png – Complete JSON result generated by the system.

Screenshot (143).png – JSON output displayed in a readable format on the UI.

Screenshot (144).png – Option to view or copy the generated JSON output.

Screenshot (151).png – Backend API running successfully and handling requests.

Screenshot (152).png – Streamlit frontend running locally and connected to the backend.

Screenshot (153).png – Full workflow showing successful issue analysis from input to output.

Screenshot (154).png – Final result screen confirming correct application behavior.

Screenshot (155).png – Overall demonstration of the working GitHub Issue AI Assistant.
### Step-by-Step Execution Screenshots

If you prefer a visual guide, step-by-step execution screenshots are available at the following Google Drive link:
https://drive.google.com/file/d/1p0RtVNFa7DPiTowxK4ZMbQQsdTN5I5PQ/view?usp=sharing







