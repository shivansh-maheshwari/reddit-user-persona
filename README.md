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

🛠 Tech Stack
  Tool	                      Purpose
Python 3.10	           Core programming language
PRAW	                 Reddit API wrapper
google-generativeai	   For Gemini LLM access
python-dotenv        	 Loads API keys from .env

⚙️ Setup Instructions
1️⃣ Clone the Repository

git clone https://github.com/shivansh-maheshwari/reddit-user-persona.git
cd reddit-user-persona

2️⃣ Create a Virtual Environment (Optional but Recommended)

python -m venv venv
# Windows

venv\Scripts\activate
# macOS/Linux
source venv/bin/activate

3️⃣ Install Dependencies

pip install -r requirements.txt

4️⃣ Configure API Keys

Create a .env file in the root folder:

REDDIT_CLIENT_ID=your_reddit_client_id
REDDIT_CLIENT_SECRET=your_reddit_client_secret
REDDIT_USER_AGENT=reddit-persona-script (by /u/your_username)
GEMINI_API_KEY=your_google_gemini_api_key

5️⃣ Run the Script

python main.py
Enter the Reddit profile URL when prompted.

📁 Output

Each run creates a file like:

kojied_persona.txt
Hungry-Move-6603_persona.txt

Each file contains:

Persona traits (interests, tone, style, values)

Post/comment IDs as citations

Clean and structured text for analysis
