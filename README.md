My Cute API
A simple, rule-based question-answering API built with Node.js and Express. It answers fun queries about fictional characters using hardcoded data as a fallback. Deployed for quick demos!
Features

Rule-based Q&A: Matches questions to predefined patterns and responds with relevant info.
Backup Data: Works offline or if external APIs are down—uses local JSON data.
Fast Deployment: Set up in under 30 seconds on Vercel or Railway.
Demo Queries: Test with questions about Layla, Vikram, Amira, and more.

Tech Stack

Node.js
Express.js
URL-encoded query parsing for questions
JSON responses

Installation

Clone the repo:textgit clone https://github.com/punithapokala01-lgtm/my-cute-api.git
cd my-cute-api
Install dependencies:textnpm install
Run locally:textnpm startServer runs on http://localhost:3000.

Usage
Send a GET request to /ask with a question parameter (URL-encoded).
Example:
texthttps://my-cute-ap-punithapokala01-lgtms-projects.vercel.app/ask?question=When%20is%20Layla%20Kawaguchi%20going%20to%20London
Response:
json{"answer": "Layla Kawaguchi is going to London in July 2026!"}
Demo Queries

Working links (tested in USA right now):
1. Layla → https://my-cute-ap-punithapokala01-lgtms-projects.vercel.app/ask?question=When%20is%20Layla%20Kawaguchi%20going%20to%20London
   → {"answer": "Layla Kawaguchi is going to London in July 2026!"}

2. Vikram → https://my-cute-ap-punithapokala01-lgtms-projects.vercel.app/ask?question=How%20many%20cars%20does%20Vikram%20Desai%20have
   → {"answer":  "I only know Layla Kawaguchi, Vikram Desai, and Amira"}
   
Data Structure
Data is stored in data.json (backup file):
{
  "people": {
    "Layla Kawaguchi": {
      "trips": [
      {
          "destination": "London",
          "date": "July 2026"
        }
      ]
    },
    "Vikram Desai": {},
    "Amira": {}
  }
}
Deployment

Vercel (Recommended): Connect GitHub repo → Deploy in seconds. Live: https://my-cute-ap-punithapokala01-lgtms-projects.vercel.app
