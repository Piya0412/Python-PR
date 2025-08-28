

Week 1 – Linux Foundation (Cloud/DevOps Focus)

Goal: Be comfortable with Linux basics + AWS CLI environment.


Daily Plan

Day 1:


Install Linux (Ubuntu / WSL).

Practice: ls, cd, pwd, mkdir, rmdir, cp, mv, rm.

Exercise: Create a folder cloud_project/ and inside it make subfolders scripts, logs, data.


Day 2:


Learn file viewing & searching: cat, head, tail, grep, find.

Exercise: Create a log file and extract error lines with grep "ERROR" logfile.txt.

Day 3:

File permissions: chmod, chown, umask.

Exercise: Create a script deploy.sh, make it executable, and run it.

Day 4:

Processes & monitoring: ps, top, htop, kill.

Exercise: Run a Python script, find its PID, and kill it.

Day 5:

Networking: ping, curl, wget, netstat.

Exercise: curl https://api.github.com → parse JSON.

Day 6:

Archiving: tar, gzip, unzip.

Exercise: Compress your project folder into a .tar.gz and extract it.

Day 7 (Mini-Project):

Write a bash script that:

Creates a backup of a folder,

Compresses it,

Uploads it to AWS S3 using AWS CLI (aws s3 cp).

Week 2 – Python Essentials for Automation

Goal: Python scripting for AWS, automation, and API calls.

Daily Plan

Day 8:

Python basics: variables, loops, functions.

Exercise: Write a script to print all files in a folder.

Day 9:

File handling: open, read, write.

Exercise: Read log.txt and count number of “ERROR” lines.

Day 10:

JSON & Config parsing.

Exercise: Save AWS credentials in JSON format, load them in Python.

Day 11:

HTTP requests with requests library.

Exercise: Call the Hugging Face Inference API (text summarizer).

Day 12:

Virtual environments (venv, pip).

Exercise: Create a virtual environment for your AI project.

Day 13:

Error handling & logging.

Exercise: Wrap your Hugging Face API script with try/except and log errors.

Day 14 (Mini-Project):

Build a Python script that:

Fetches text from a file,

Sends it to Hugging Face API for summarization,

Saves the summary in a new file.

Week 3 – Cloud Automation + Deployment Basics

Goal: Use Python + AWS SDK (boto3) + deployment frameworks.

Daily Plan

Day 15:

Install & configure AWS CLI.

Practice: aws s3 ls, aws ec2 describe-instances.

Day 16:

AWS SDK (boto3) basics: list S3 buckets.

Exercise: Write Python code to upload & download files from S3.

Day 17:

EC2 automation with boto3.

Exercise: Write a script to start/stop EC2 instances.

Day 18:

Deploy a small model to SageMaker JumpStart (pre-trained).

Exercise: Call the SageMaker endpoint from Python.

Day 19:

Secure API deployment: FastAPI basics.

Exercise: Create a FastAPI endpoint /summarize returning static text.

Day 20:

API Gateway + Lambda (theory + practice via AWS console).

Exercise: Deploy a simple Lambda (Python) → call via API Gateway URL.

Day 21 (Mini-Project):

Build a Python tool that:

Uploads text to S3,

Triggers Lambda,

Lambda calls Hugging Face API,

Saves summary back to S3.

Week 4 – Generative AI Deployment Demos

Goal: Deploy real generative AI apps with Streamlit + SageMaker/Bedrock.

Daily Plan

Day 22:

Install Streamlit & build your first app.

Exercise: Simple text input → echo output.

Day 23:

Integrate Hugging Face API with Streamlit.

Exercise: Build a summarizer app.

Day 24:

Deploy Bedrock model (text generation).

Exercise: Call Bedrock API with Python, show response in console.

Day 25:

Secure app with AWS Cognito / IAM roles (basic).

Day 26:

Ollama (local inference).

Exercise: Run ollama run llama2 locally and query it.

Day 27:

Polly (Text-to-Speech).

Exercise: Convert Bedrock output into speech.

Day 28:

Monitoring with CloudWatch.

Exercise: Log API usage of your model endpoint.

Day 29 (Mini-Project):

Build a Streamlit chatbot app that:

Uses Bedrock (or Hugging Face if Bedrock not available) for responses,

Converts response to audio via Polly,

Logs all conversations in S3.

Day 30 (Capstone Project):

End-to-End Generative AI Deployment:

Deploy a summarizer/chatbot on SageMaker,

Expose it via API Gateway,

Create a Streamlit frontend,

Log interactions to S3 + CloudWatch.