# EduMind - AI Study Assistant

A comprehensive AI-powered study assistant that helps students upload documents, generate summaries, create study notes, and take quizzes.

## Features

- **User Authentication**: Secure registration and login system
- **Document Upload**: Support for PDF, DOCX, and TXT files
- **AI Summarization**: Generate concise summaries using OpenAI GPT
- **Study Notes**: Create structured study notes from uploaded documents
- **Quiz Generation**: Generate multiple-choice quizzes from document content
- **User Dashboard**: Track all your documents, summaries, notes, and quizzes

## Tech Stack

### Backend
- **Python Flask**: Web framework
- **SQLAlchemy**: Database ORM
- **Flask-JWT-Extended**: Authentication
- **OpenAI API**: AI-powered content generation
- **PyPDF2**: PDF text extraction
- **python-docx**: DOCX text extraction

### Frontend
- **HTML5/CSS3**: Modern responsive design
- **JavaScript**: API integration and user interactions
- **Poppins Font**: Clean typography

## Installation & Setup

### Prerequisites
- Python 3.7+
- pip (Python package manager)

### 1. Clone the Repository
```bash
git clone <repository-url>
cd edumind
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Environment Configuration
Create a `.env` file in the root directory:
```env
SECRET_KEY=your-secret-key-here
JWT_SECRET_KEY=your-jwt-secret-key-here
DATABASE_URL=sqlite:///edumind.db
OPENAI_API_KEY=your-openai-api-key-here
```

### 4. Run the Application
```bash
python run.py
```

The application will be available at:
- **Frontend**: http://localhost:5000
- **API**: http://localhost:5000/api

## API Endpoints

### Authentication
- `POST /api/register` - User registration
- `POST /api/login` - User login

### Document Processing
- `POST /api/upload-summarize` - Upload file and generate summary
- `POST /api/generate-notes` - Generate study notes from document
- `POST /api/generate-quiz` - Generate quiz from document

### User Data
- `GET /api/user/documents` - Get user's documents
- `GET /api/user/summaries` - Get user's summaries
- `GET /api/user/notes` - Get user's notes
- `GET /api/user/quizzes` - Get user's quizzes

## Usage

1. **Register/Login**: Create an account or login to access features
2. **Upload Documents**: Upload PDF, DOCX, or TXT files
3. **Generate Content**: 
   - Get AI-generated summaries
   - Create structured study notes
   - Generate practice quizzes
4. **Track Progress**: View all your uploaded documents and generated content

## File Structure

```
edumind/
├── app.py                 # Main Flask application
├── config.py             # Configuration settings
├── run.py                # Startup script
├── requirements.txt      # Python dependencies
├── api.js               # Frontend API client
├── uploads/             # Uploaded files storage
├── static/              # Static frontend files
├── *.html              # Frontend pages
└── *.css               # Stylesheets
```

## Configuration

### OpenAI API Setup
1. Get an API key from [OpenAI](https://platform.openai.com/)
2. Add it to your `.env` file as `OPENAI_API_KEY`
3. Without this key, AI features will show placeholder messages

### Database
- Default: SQLite database (`edumind.db`)
- Change `DATABASE_URL` in `.env` for other databases
- Tables are created automatically on first run

## Development

### Running in Development Mode
```bash
python run.py
```

### Production Deployment
For production deployment, consider:
- Using a production WSGI server (Gunicorn)
- Setting up a proper database (PostgreSQL/MySQL)
- Configuring environment variables securely
- Setting up HTTPS

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

This project is licensed under the MIT License.

## Support

For issues and questions, please create an issue in the repository.
