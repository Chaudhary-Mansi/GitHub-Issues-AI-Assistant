# GitHub-Issues-AI-Assistant

## Overview

This project is an AI-powered assistant that fetches,stores, and retrieves GitHub issues using LangChain, AstraDB Vector Store, and OpenAI models. It allows users to search GitHub issues using natural language queries and interact with them through an AI agent.

## Features

✅ Fetch GitHub Issues: Retrieves issues from a specified GitHub repository using GitHub API.

✅ Vector Storage: Stores issues in AstraDB Vector Store for fast semantic search.

✅ AI-Powered Search: Uses OpenAI’s language models to retrieve relevant GitHub issues.

✅ Interactive Q&A: Allows users to ask questions about GitHub issues and get AI-driven responses.

## Setup Instructions

### 1. Install Dependencies

Ensure Python is installed, then install the required packages:

pip install langchain-openai langchain-astradb python-dotenv requests

### 2. Environment Variables

Create a .env file in the project root and add the following:

ASTRA_DB_API_ENDPOINT=<your_astra_db_endpoint>

ASTRA_DB_APPLICATION_TOKEN=<your_astra_db_token>

ASTRA_DB_KEYSPACE=<your_astra_db_keyspace>

OPENAI_API_KEY=<your_openai_api_key>

GITHUB_TOKEN=<your_github_api_token>

### 3. Run the Script

Execute the script with:

python script.py
It will prompt if you want to update GitHub issues.
Then, you can ask questions about stored issues interactively.

### Usage

### 1. Fetching and Storing GitHub Issues

The script will prompt:
Mathematica

Do you want to update the issues? (y/N):
If 'y' is entered, it will:
Fetch issues from the repository (mention the repository url).
Store them in AstraDB for retrieval.

### 2. Asking Questions About Issues

Enter a question related to GitHub issues.
The AI will provide a response based on the stored issues.
Type 'q' to quit.

### Customization

Modify the owner and repo variables to fetch issues from a different repository.
Change search_kwargs={"k": 3} to adjust the number of retrieved results.
Modify fetch_github_issues() to retrieve other GitHub data (e.g., pull requests).

### Code Structure

📂 GitHub Issues AI Assistant  
 ├── script.py               # Main script  
 ├── github.py               # Fetches GitHub issues  
 ├── note.py                 # Note-taking tool  
 ├── .env                    # Environment variables  
 ├── README.md               # Project documentation  
 └── requirements.txt        # Dependencies  
