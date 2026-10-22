# College FAQ Chatbot

A simple FAQ chatbot that answers common college questions for students. It's built with **FastAPI** and **RapidFuzz**, and it matches what the student types against ready made answers stored in `backend/data/intents.json`.

If the bot is confident, it will give the answer. If it is not sure, it will say so instead of guessing.

---

## 👥 Team
- Asif Siddique
- Mayank Kumar

---

## How to Run

**1. Install dependencies**
```bash
pip install -r requirements.txt
```

**2. Start the server**
```bash
uvicorn backend.app.main:app --reload --port 8000
```

**3. Open in browser**

Go to http://localhost:8000 to use the chat.

---

## Running Tests
```bash
pip install -r requirements-dev.txt
python -m pytest
```

---

## For Adding or Updating Answers
All the knowledge of bot is in `backend/data/intents.json`. Each entry looks like this...

```json
{
  "tag": "fees_info",
  "patterns": ["How much is the tuition fee?", "Fees structure", "Fee payment"],
  "responses": ["The annual tuition fee for B.Sc. Computer Science is approximately 24,000 to 31,000 Rs"]
}
```

---

## Note for my Group partner Mayank (adding patterns)
1. **Think like a student** Add short phrases people actually type, like "Fees"...
2. **No duplicates** Don't put the same pattern under two different tags.
3. **Be specific** Add patterns for each topic so the bot can tell them apart.
4. **Low accuracy** Try adjusting the match threshold, filler words and synonyms in the backend config.
5. **Stuck on the JSON database part?** Message me or meet me in college...