# Full Stack Contact List Application

## Project Overview
A full-stack contact management application built with Python, React, Flask, and MySQL.

## Technologies Used
- **Frontend**: React
- **Backend**: Flask (Python)
- **Database**: MySQL
- **API**: RESTful Flask API

## Prerequisites
- Python 3.8+
- Node.js 14+
- MySQL 8.0+
- pip
- npm

## Setup Instructions

### Backend Setup
1. Clone the repository
2. Create a virtual environment
```bash
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```

3. Install Python dependencies
```bash
pip install -r requirements.txt
```

4. Database Configuration
- Create MySQL database
- Update `config.py` with database credentials
```python
DB_CONFIG = {
    'host': 'localhost',
    'user': 'your_username',
    'password': 'your_password',
    'database': 'contact_list_db'
}
```

5. Run database migrations
```bash
flask db upgrade
```

6. Start Flask server
```bash
flask run
```

### Frontend Setup
1. Navigate to frontend directory
```bash
cd frontend
npm install
```

2. Start React development server
```bash
npm start
```

## Features
- Create, Read, Update, Delete (CRUD) contacts
- Search and filter contacts
- Responsive design
- Form validation

## API Endpoints
- `GET /contacts`: Retrieve all contacts
- `POST /contacts`: Create new contact
- `PUT /contacts/<id>`: Update existing contact
- `DELETE /contacts/<id>`: Delete contact

## Database Schema
```sql
CREATE TABLE contacts (
    id INT PRIMARY KEY AUTO_INCREMENT,
    first_name VARCHAR(50) NOT NULL,
    last_name VARCHAR(50) NOT NULL,
    email VARCHAR(100) UNIQUE,
    phone VARCHAR(20),
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

## Environment Variables
Create a `.env` file in the root directory:
```
FLASK_APP=app.py
FLASK_ENV=development
DATABASE_URL=mysql://username:password@localhost/contact_list_db
```

## Testing
- Backend: `python -m pytest`
- Frontend: `npm test`

## Deployment
Recommended platforms: Heroku, AWS, DigitalOcean

## Contributing
1. Fork the repository
2. Create feature branch
3. Commit changes
4. Push to branch
5. Create pull request

## License
MIT License

Link: https://github.com/nextking12/FullStackPython_Flask_React_SQLite.git
