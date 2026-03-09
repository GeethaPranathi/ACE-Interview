# ACE AI-Interview

ACE AI-Interview is an AI-powered platform designed to help users master their dream job interviews. It simulates interviews, analyzes performance, and provides personalized feedback using the Google Gemini API.

## 🚀 Features
- **Resume Parsing**: Extract key skills and experience from PDF resumes.
- **AI Question Generation**: Generates relevant interview questions based on the candidate's resume and job description.
- **Performance Analysis**: Provides structured feedback on user responses to improve interview skills.
- **Modern UI**: A responsive and intuitive interface built with Next.js.

## 🛠️ Tech Stack
- **Frontend**: Next.js (React), Tailwind CSS, Redux.
- **Backend**: Python (Flask).
- **AI engine**: Google Gemini API.
- **Deployment**: Vercel (Frontend), Render/Railway (Backend).

## 📂 Project Structure
```text
ACE-Interview/
├── UI-main/
│   ├── UI-main/           # Next.js Frontend
│   └── llm-api-main/
│       └── llm-api-main/  # Flask Backend
├── .gitignore             # Root git ignore
└── README.md              # Project documentation
```

## 💻 Local Development

### 1. Backend Setup
1.  Navigate to the backend directory:
    ```bash
    cd UI-main/llm-api-main/llm-api-main
    ```
2.  Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```
3.  Create a `.env` file and add your Gemini API Key:
    ```text
    GEMINI_API_KEY=your_api_key_here
    ```
4.  Run the server:
    ```bash
    python app.py
    ```
    *Backend runs on `http://localhost:5000`*

### 2. Frontend Setup
1.  Navigate to the frontend directory:
    ```bash
    cd UI-main/UI-main
    ```
2.  Install dependencies:
    ```bash
    npm install
    ```
3.  Create a `.env.local` file:
    ```text
    NEXT_PUBLIC_API_BASE_URL=http://localhost:5000
    ```
4.  Run the development server:
    ```bash
    npm run dev
    ```
    *Frontend runs on `http://localhost:3000`*

## 🌐 Deployment

### Backend (Render/Railway)
- **Root Directory**: `UI-main/llm-api-main/llm-api-main`
- **Build Command**: `pip install -r requirements.txt`
- **Start Command**: `gunicorn app:app`
- **Environment Variables**: Add `GEMINI_API_KEY`.

### Frontend (Vercel)
- **Root Directory**: `UI-main/UI-main`
- **Framework Preset**: Next.js
- **Environment Variables**: Set `NEXT_PUBLIC_API_BASE_URL` to your deployed backend URL.

## 📄 License
This project is licensed under the MIT License.