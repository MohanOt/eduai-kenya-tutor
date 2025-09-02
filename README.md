
# 📘 EduAI – AI Study Buddy

An **AI-powered flashcard generator** that transforms raw study notes into interactive quiz cards, helping students revise smarter and faster.  
Built with **Flask + MySQL + Hugging Face AI + HTML/CSS/JS**.  

---

## 🚀 Features
- 📝 Paste study notes → get **quiz questions instantly**
- 🤖 AI-powered (Hugging Face Question-Answering API)
- 🎴 Interactive **flip cards** (HTML/CSS/JS)
- 💾 Save & reuse flashcards (MySQL backend)
- 🌍 Beginner-friendly but highly impactful

---

## 🛠 Tech Stack
- **Frontend:** HTML5, CSS3, JavaScript  
- **Backend:** Python (Flask)  
- **Database:** MySQL  
- **AI:** Hugging Face Transformers API  

---

## ⚙️ How It Works
1. User pastes study notes into the app.  
2. Flask backend sends notes to Hugging Face API: *“Generate 5 quiz questions.”*  
3. JS frontend creates interactive flip cards.  
4. Flashcards stored in MySQL for reuse and tracking.  

---

## 📂 Repository Structure
```

EduAI-StudyBuddy/
│── backend/
│   ├── app.py              # Flask app
│   ├── models.py           # DB models
│   ├── routes.py           # API endpoints
│   ├── requirements.txt    # Python dependencies
│
│── frontend/
│   ├── index.html          # Main UI
│   ├── style.css           # Styling
│   ├── script.js           # Flashcard logic
│
│── database/
│   ├── schema.sql          # MySQL schema
│
│── docs/
│   ├── README.md           # Documentation
│
│── .gitignore
│── config.example.json
│── LICENSE

````

---

## 📸 Demo
- Paste notes → AI generates flashcards  
- Click cards to flip & view answers  
- Save decks for future revision  

*(Screenshots or demo GIFs can be added here)*

---

## 📈 Market Gap
- Current flashcard apps (like Quizlet) require **manual entry**  
- Few tools convert **raw notes → study questions automatically**  
- Global **EdTech market = $350B+ by 2025**, with rising demand for AI learning  

---

## 💡 Why EduAI
✅ Beginner-friendly but full-stack learning  
✅ Real-world EdTech use case  
✅ Combines **AI + interactivity + database storage**  
✅ Scalable into mobile apps & e-learning platforms  

---

## 🔮 Roadmap
- [ ] User accounts & personalized decks  
- [ ] Multiple-choice & difficulty-based generation  
- [ ] Mobile app version  
- [ ] Teacher dashboard + classroom integration  

---

## 🤝 Our Ask
We are seeking **mentorship, technical support, and seed funding** to:  
- Deploy MVP for student testing  
- Add personalization features  
- Scale to Android & iOS  
- Partner with schools & EdTech firms  

---

## 🧑‍💻 Setup & Installation
1. Clone the repo:  
   ```bash
   git clone https://github.com/your-username/EduAI-StudyBuddy.git
   cd EduAI-StudyBuddy
````

2. Backend setup:

   ```bash
   cd backend
   pip install -r requirements.txt
   python app.py
   ```
3. Database setup:

   ```bash
   mysql -u root -p < database/schema.sql
   ```
4. Frontend setup:
   Open `frontend/index.html` in your browser.

---

## 📜 License

MIT License – free to use and modify for educational purposes.

---

## ✨ Contributors

* \Mohan Otieno – Project Lead
* Open for contributions 🎉

---

## 🙌 Acknowledgments

* Hugging Face for NLP APIs
* Flask & MySQL community
* Students who inspired EduAI


# This was my prompt to Lovable


EduAI – Master Prompt for Lovable
Build EduAI – a full-stack AI-powered learning assistant tailored for the Kenyan secondary school curriculum (SDG 4: Quality Education). The platform should support free and premium students, provide personalized AI tutoring, an AI-powered flashcard generator, and integrate payments via IntaSend.
Frontend (React + Tailwind + HTML5/CSS/JS for Flashcards)
• Landing page with Kenyan-inspired theme (forest green, amber, blue).
• Signup/Login pages (Supabase Auth).
• Student dashboard with free lessons, AI Study Buddy chat, and Flashcard Generator.
• Flashcard Generator: textarea input → Flask → Hugging Face → 5 Q&A flashcards with flip animations (CSS/JS).
• Save & retrieve flashcards from database.
• Premium features page: mock exams, progress tracking graphs (charts).
• IntaSend “Upgrade to Premium” button.
• Responsive, mobile-first design with smooth animations.
Backend
Supabase (Postgres + RLS + Auth)
• Authentication: email/password login.
• Tables with RLS: profiles, progress_records, mock_exams, mock_exam_attempts, flashcards.
• Flashcards table with CRUD access limited to owner.
Flask Microservice
• Endpoint /generate-flashcards → Hugging Face API.
• Endpoint /save-flashcards → Save flashcards to DB.
• Endpoint /get-flashcards → Retrieve saved flashcards.
• Endpoint /ask-tutor → Connects to OpenAI tutoring API.
• Endpoint /payments/webhook → Handles IntaSend callbacks.
AI Study Buddy
• Chat interface powered by OpenAI API.
• Answers curriculum-related questions.
• Explains concepts step by step.
• Generates quizzes dynamically.
• Provides personalized study help. 

Payments (IntaSend Integration)
• Public Key: ISPubKey_live_5796eb2a-3e7c-4e12-837d-eee27c2198f0
• Upgrade flow: button → checkout link → webhook updates is_premium=true.
• Pricing: KES 500 one-time payment.
• Supports parents/teachers paying for multiple students.
Repo Structure

eduai/
│
├── frontend/                # React + Tailwind frontend
│   ├── public/              # Static assets
│   ├── src/
│   │   ├── components/      # Navbar, Flashcards, Charts, PayButton
│   │   ├── pages/           # Landing, Dashboard, StudyBuddy, Premium
│   │   ├── hooks/           # Custom React hooks
│   │   ├── utils/           # Helpers (API calls, auth utils)
│   │   └── App.tsx
│   ├── package.json
│   └── tailwind.config.js
│
├── backend/                 # Flask + Supabase microservice
│   ├── app.py               # Flask entry point
│   ├── routes/
│   │   ├── flashcards.py    # Hugging Face integration
│   │   ├── payments.py      # IntaSend webhook
│   │   └── tutor.py         # OpenAI tutoring API
│   ├── models/              # SQLAlchemy models (if MySQL used)
│   ├── requirements.txt
│   └── config.py
│
├── supabase/                # Supabase migrations + schema
│   ├── migrations/
│   │   ├── 001_init.sql     # profiles, exams, attempts
│   │   └── 002_flashcards.sql
│   └── policies.sql         # RLS policies
│
├── docs/                    # Documentation
│   ├── README.md
│   ├── API.md
│   └── DEPLOYMENT.md
│
└── .gitignore

Deliverables
• Fully working React + Tailwind frontend.
• Flask backend with Hugging Face + OpenAI API integration.
• Supabase backend with secure RLS schema.

Pitch dec link: https://gamma.app/docs/Study-Buddy-Flashcard-Generator-tccvgwued99dkx6
• Flashcard Generator (interactive, stored in DB).
• IntaSend payments integrated with premium upgrade.
• Deploy frontend on Vercel, backend on Render/Heroku, database & auth via Supabase.
