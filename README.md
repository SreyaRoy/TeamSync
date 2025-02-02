# TeamSync: AI-Powered Daily Standup Bot

## 📌 What It Does
- Collects **daily standup updates** from team members via API.
- Uses **Natural Language Processing (NLP)** to analyze updates, highlight blockers, and track progress.
- Generates a **concise AI-powered summary** of all standups.
- Automatically sends the **summary report to a Slack channel**.

## 📌 Tech Stack
- **Backend:** Flask (Python)
- **AI/NLP:** OpenAI API (for summarization) or Spacy
- **Database:** SQLite (for simplicity) or PostgreSQL (for scalability)
- **Deployment:** Render or Railway (simple & scalable)

## 📌 How to Run Locally
### 1️⃣ Clone the Repository
```bash
 git clone https://github.com/yourusername/TeamSync.git
 cd TeamSync
```

### 2️⃣ Install Dependencies
```bash
 pip install -r requirements.txt
```

### 3️⃣ Set Up Environment Variables
Create a `.env` file and add your OpenAI API key:
```env
 OPENAI_API_KEY=your_api_key_here
```

### 4️⃣ Run the Application
```bash
 python teamsync_bot.py
```

### 5️⃣ Test the API Endpoints
- **Submit a Standup Update:**
```bash
curl -X POST http://127.0.0.1:5000/standup -H "Content-Type: application/json" -d '{"user":"John", "update":"Completed feature A, blocked on API access"}'
```
- **Generate a Summary:**
```bash
curl -X GET http://127.0.0.1:5000/summary
```

## 📌 Deployment
### Deploy on Render (Recommended)
1. **Push your code to GitHub**
2. **Sign up on [Render](https://render.com/)**
3. **Create a new Web Service → Connect GitHub Repo**
4. **Set Build Command:**
   ```bash
   pip install -r requirements.txt
   ```
5. **Set Start Command:**
   ```bash
   gunicorn -w 4 -b 0.0.0.0:5000 teamsync_bot:app
   ```
6. **Deploy & Get Live URL!**

## 📌 Future Improvements
- Add authentication for standup submissions.
- Enhance AI summarization with fine-tuned models.
- Integrate directly with Slack via a bot webhook.

🚀 **Let's streamline team standups with AI!**


