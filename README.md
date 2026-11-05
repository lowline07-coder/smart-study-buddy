# 📚 Smart Study Buddy

**Smart Study Buddy** is an AI-powered study assistant that turns any topic into a complete, structured study guide in seconds. Enter a topic, pick a difficulty level, and the app uses Google Gemini (via LangChain) to generate an explanation, examples, practice MCQs, interview questions, and a quick summary — all rendered neatly in a Streamlit web interface.

It is built for students, self-learners, and job seekers who want fast, level-appropriate revision material without searching through multiple sources.

---

## ✨ Project Features

- Topic input
- Difficulty selection (Easy / Medium / Hard)
- Explanation tailored to the chosen difficulty
- Simple example
- Real-life example
- 5 MCQs with options and correct answers
- 5 Interview questions
- Summary in bullet points

## 🛠️ Technology Stack

- Python 3.11+
- Google Gemini API
- LangChain
- Streamlit
- python-dotenv

## 📁 Folder Structure

```
Smart_Study_Buddy/
├── app.py            # Streamlit UI and LangChain chain
├── prompts.py        # Prompt template for study material
├── .env              # API key (never commit this)
├── requirements.txt  # Python dependencies
└── README.md         # Project documentation
```

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/<your-username>/smart-study-buddy.git
cd smart-study-buddy
```

### 2. Create a virtual environment (recommended)

```bash
python -m venv venv
source venv/bin/activate      # On Windows: venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Add your Gemini API key

Get a free key from [Google AI Studio](https://aistudio.google.com/app/apikey), then edit the `.env` file:

```
GOOGLE_API_KEY=your_gemini_api_key_here
```

### 5. Run the app

```bash
streamlit run app.py
```

The app opens at `http://localhost:8501`.

## 🧠 How It Works

1. The user enters a topic and selects a difficulty level in the Streamlit UI.
2. `prompts.py` provides a structured prompt template with the topic and difficulty filled in.
3. LangChain pipes the prompt into the Gemini model (`gemini-2.5-flash-lite`).
4. The model returns Markdown, which Streamlit renders as the final study material.

## 🔐 Security Note

Never upload your `.env` file to GitHub. It is already listed in `.gitignore`.

## 🔮 Future Improvements

- Download study material as PDF
- Interactive quiz mode with scoring
- Save and revisit past topics
- Support for multiple languages

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

