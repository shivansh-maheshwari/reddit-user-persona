# 📘 reddit-user-persona

A powerful script that scrapes Reddit user data and generates insightful user personas using Google's **Gemini (Generative AI)** model.

---

## 🚀 Function

This tool:
- Accepts a Reddit user profile URL as input
- Scrapes the user's public **posts** and **comments**
- Generates a **detailed, qualitative persona** using Gemini (Google's LLM)
- Cites the exact post/comment used to extract each piece of persona information
- Outputs the persona as a `.txt` file

---

## 🌟 Features

- 🔗 Input: Accepts Reddit profile URLs like:
  - `https://www.reddit.com/user/kojied/`
  - `https://www.reddit.com/user/Hungry-Move-6603/`

- 🔍 Scraping:
  - Fetches latest **posts** and **comments** using Reddit's API

- 🤖 Persona Generation:
  - Uses Gemini (Google LLM) to analyze text and build a personality profile

- 📌 Citation:
  - Cites specific Post or Comment IDs used to generate each trait

- 📄 Output:
  - Saves the full persona report with citations to a `.txt` file named after the user

---

## 🧠 Example Outputs

For example, given:

https://www.reddit.com/user/kojied/

The script generates a `kojied_persona.txt` file, which might include:

```txt
1. Interests & Hobbies:
Frequently discusses anime, RPG gaming, and fan theories.
Cited from: [Comment ID: abc123], [Post ID: xyz789]

2. Tone & Attitude:
Casual and witty with occasional sarcasm.
Cited from: [Comment ID: jkl456]
The same applies for:

https://www.reddit.com/user/Hungry-Move-6603/
→ output: Hungry-Move-6603_persona.txt

Tech Stack
Python 3
PRAW (Reddit API Wrapper)
Google Generative AI (Gemini Pro)
dotenv (.env file for API keys)
Setup Instructions
1. Clone this repository
git clone https://github.com/tusharharyana/reddit-persona-generator.git
cd reddit-persona-generator
2. (Optional) Create a virtual environment
python -m venv venv
venv\Scripts\activate
3. Install the dependencies
pip install -r requirements.txt
4. Create a .env file
REDDIT_CLIENT_ID=your_reddit_client_id
REDDIT_CLIENT_SECRET=your_reddit_client_secret
REDDIT_USER_AGENT=your_user_agent_string
GEMINI_API_KEY=your_gemini_api_key
How to Use
Run the script and enter a Reddit profile URL:

python generate_persona.py
Example input : https://www.reddit.com/user/kojied/

LLM Prompt (Used with Gemini Pro)
The LLM prompt was designed to return structured personas and include references to specific posts/comments used for inferen
