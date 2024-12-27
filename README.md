# News App

## Overview
The News App is a full-stack web application that provides users with the latest news articles. It is designed to deliver a seamless user experience with a React-powered frontend and a Django-based backend. The application uses PostgreSQL as its database for efficient data storage and retrieval.

## Features

### Frontend:
- Developed using React.
- Responsive design to support various devices.
- User-friendly interface for browsing news articles.
- Pagination and search functionality.

### Backend:
- Built using Django and Django REST Framework (DRF).
- API endpoints to manage and fetch news articles.
- User authentication and authorization using Django's built-in authentication system.

### Database:
- PostgreSQL is used as the primary database to store news articles and user data.

## Architecture
The application is divided into three primary services:

1. **Frontend**:
   - Technology: React
   - Directory: `frontend/`
   - Port: 3000

2. **Backend**:
   - Technology: Django
   - Directory: `backend/`
   - Port: 8000

3. **Database**:
   - Technology: PostgreSQL
   - Port: 5432

All services are containerized using Docker and orchestrated using Docker Compose.

## Installation and Setup

### Prerequisites:
- Docker and Docker Compose installed on your system.
- Node.js and npm (for frontend development only).
- Python (for backend development only).

### Steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/obaidallah1/newsapp.git
   cd newsapp
   ```

2. Create a `.env` file in the project root for environment variables:
   ```bash
   POSTGRES_USER=postgres
   POSTGRES_PASSWORD=postgres
   POSTGRES_DB=postgres
   DB_HOST=db
   ```

3. Build and start the Docker Compose stack:
   ```bash
   docker-compose up --build
   ```

4. Access the application:
   - Frontend: [http://localhost:3000](http://localhost:3000)
   - Backend: [http://localhost:8000](http://localhost:8000)

## File Structure
```
news_app/
├── frontend/          # React frontend
├── backend/           # Django backend
├── docker-compose.yml # Docker Compose configuration
├── .env               # Environment variables
├── README.md          # Project documentation
```

## Development

### Frontend:
1. Navigate to the `frontend/` directory.
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the development server:
   ```bash
   npm start
   ```

### Backend:
1. Navigate to the `backend/` directory.
2. Set up a virtual environment:
   ```bash
   python -m venv env
   source env/bin/activate  # On Windows, use `env\Scripts\activate`
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Run migrations and start the server:
   ```bash
   python manage.py migrate
   python manage.py runserver
   ```

## Contributing
1. Fork the repository.
2. Create a feature branch:
   ```bash
   git checkout -b feature/<feature-name>
   ```
3. Commit your changes and push to your fork.
4. Open a pull request.

## License
This project is licensed under the [MIT License](LICENSE).

## Acknowledgements
- React and Django communities for their amazing frameworks.
- Docker for making containerization seamless.

