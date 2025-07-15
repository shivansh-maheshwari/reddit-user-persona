# Reddit User Persona

A powerful script that scrapes Reddit user data and generates insightful user personas using Google's **Gemini (Generative AI)** model.

---

## Features

- Input: Reddit user profile URL
- Scrapes latest posts and comments from the user
- Uses Gemini (Google's LLM) to analyze behavior
- Outputs a structured User Persona in `.txt` format
- Cites which post or comment supports each trait
- Follows PEP-8 coding guidelines

## Tech Stack
---
| Tool                                                                  | Purpose                        |
| --------------------------------------------------------------------- | ------------------------------ |
| Python 3.10                                                           | Core programming language      |
| [PRAW](https://praw.readthedocs.io/)                                  | Reddit API wrapper             |
| [google-generativeai](https://github.com/google/generative-ai-python) | For Gemini LLM access          |
| [python-dotenv](https://pypi.org/project/python-dotenv/)              | Loads API keys from `.env`     |


## Setup Instructions

### 1. Clone this repository

```bash
git clone https://github.com/shivansh-maheshwari/reddit-user-persona.git
cd reddit-user-persona
```

### 2. (Optional) Create a virtual environment
```bash
python -m venv venv
venv\Scripts\activate
```
### 3. Install the dependencies
```bash
pip install -r requirements.txt
```

### 4. Create a .env file
```bash
REDDIT_CLIENT_ID=your_reddit_client_id
REDDIT_CLIENT_SECRET=your_reddit_client_secret
REDDIT_USER_AGENT=your_user_agent_string
GEMINI_API_KEY=your_gemini_api_key
```

## How to Use

Run the script and enter a Reddit profile URL:
```bash
python main.py
```

Example input : `https://www.reddit.com/user/kojied/`

## LLM Prompt (Used with Gemini)

The LLM prompt was designed to return structured personas and include references to specific posts/comments used for inference.

## Output

Each run creates a file like:

kojied_persona.txt
Hungry-Move-6603_persona.txt

Each file contains:  

- Persona traits (interests, tone, style, values)  
- Post/comment IDs as citations  
- Clean and structured text for analysis  
