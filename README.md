# QuizAppAI

QuizAppAI is a web application that allows users to generate quizzes automatically from PDF documents using AI. Users can upload a PDF, customize quiz settings, and receive a set of questions generated from the document content.

## Features

- User authentication (register, login, logout)
- Upload PDF files
- AI-powered quiz generation from PDF content
- Customizable quiz settings (number of questions, difficulty, etc.)
- Take quizzes and view results
- Admin dashboard for managing users and quizzes

## Tech Stack

- **Backend:** Flask, SQLAlchemy, Flask-Login
- **Frontend:** HTML, CSS, JavaScript (Jinja2 templates)
- **Database:** MySQL (configurable)
- **AI Service:** Pluggable quiz generator (Gemini or fallback)
- **PDF Parsing:** PyPDF2

## Getting Started

### Prerequisites

- Python 3.8+
- MySQL server (or compatible database)
- [pipenv](https://pipenv.pypa.io/en/latest/) or `pip`
- (Optional) [Node.js](https://nodejs.org/) for frontend tooling

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/YOUR-USERNAME/YOUR-REPO.git
   cd Quiz-Generator-master
   ```

2. **Create and activate a virtual environment:**
   ```bash
   python -m venv venv
   venv\Scripts\activate  # On Windows
   # source venv/bin/activate  # On Mac/Linux
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up environment variables:**
   Create a `.env` file in the root directory:
   ```
   SECRET_KEY=your-secret-key
   DATABASE_URL=mysql+pymysql://username:password@localhost/quiz
   ```

5. **Initialize the database:**
   ```bash
   flask db upgrade
   ```

6. **Run the application:**
   ```bash
   flask run
   ```

7. **Access the app:**
   Open [http://localhost:5000](http://localhost:5000) in your browser.

## Usage

1. Register a new account or log in.
2. Upload a PDF document.
3. Customize your quiz settings.
4. Wait for the AI to generate your quiz.
5. Take the quiz and view your results.

## Project Structure

```
Quiz-Generator-master/
│
├── app/
│   ├── static/
│   ├── templates/
│   └── ...
├── backend/
│   ├── appl.py
│   ├── models.py
│   └── services/
├── uploads/
├── requirements.txt
├── README.md
└── .env.example
```

## Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.

## License

[MIT](LICENSE)

## Acknowledgements

- Flask
- PyPDF2
- SQLAlchemy
- Gemini AI (or fallback generator)
