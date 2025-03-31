# Resume Analyzer

A full-stack application that analyzes resumes using AI and NLP techniques. Built with Next.js, Rust, and Python made for learning purposes.

## Features

- Resume upload and parsing
- AI-powered resume analysis
- User authentication and authorization
- Real-time analysis results
- Modern, responsive UI

## Tech Stack

- **Frontend**: Next.js 14 (App Router), TypeScript, TailwindCSS
- **Backend**: Rust (Axum)
- **NLP Service**: Python (FastAPI)
- **Database**: PostgreSQL(Supabase)
- **Containerization**: Docker & Docker Compose

## Prerequisites

- Docker and Docker Compose
- Node.js 18+ (for local development)
- Rust (for local development)
- Python 3.11+ (for local development)
- PostgreSQL (for local development)

## Getting Started

1. Clone the repository:
```bash
git clone https://github.com/Kingdawnage/resume-analyzer.git
cd resume-analyzer
```

2. Create environment files:
```bash
# Copy example environment files
cp ra-frontend/.env.example ra-frontend/.env.local
cp ra-backend/.env.example ra-backend/.env
cp nlp-service/.env.example nlp-service/.env
```

3. Update the environment variables in each `.env` file with your configuration.

4. Start the application using Docker Compose:
```bash
docker-compose up --build
```

The application will be available at:
- Frontend: http://localhost:3000
- Backend API: http://localhost:8080
- NLP Service: http://localhost:8000

## Development

### Running Services Locally

1. **Frontend Development**:
```bash
cd ra-frontend
npm install
npm run dev
```

2. **Backend Development**:
```bash
cd ra-backend
cargo run
```

3. **NLP Service Development**:
```bash
cd nlp-service
python -m venv venv
source venv/bin/activate  # On Windows: .\venv\Scripts\activate
pip install -r requirements.txt
python -m app.main
```

### Project Structure

```
resume-analyzer/
├── ra-frontend/          # Next.js frontend application
├── ra-backend/           # Rust backend API
├── nlp-service/          # Python NLP service
└── docker-compose.yml    # Docker Compose configuration
```

## API Documentation

### Backend API Endpoints

- `POST /api/auth/login` - User login
- `POST /api/auth/register` - User registration
- `POST /api/resumes/resume` - Upload resume
- `GET /api/resumes` - Get user's resumes
- `GET /api/resumes/:id` - Get specific resume
- `GET /health` - Health check endpoint

### NLP Service Endpoints

- `POST /analyze_resume/` - Analyze resume text
- `GET /health` - Health check endpoint

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [Next.js](https://nextjs.org/)
- [Rust](https://www.rust-lang.org/)
- [FastAPI](https://fastapi.tiangolo.com/)
- [PostgreSQL](https://www.postgresql.org/) 