# Student Attendance System

A Flask-based web application for tracking student attendance.

## Features

- Add, update, and delete student records
- Mark and track daily attendance
- Generate monthly attendance reports
- Export data to Excel

## Setup

### Local Development

1. Clone the repository
2. Create a virtual environment:
   ```bash
   python -m venv venv
   ```
3. Activate the virtual environment:
   - Windows: `venv\Scripts\activate`
   - Unix/Mac: `source venv/bin/activate`
4. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
5. Create a `.env` file based on `env.example`
6. Run the application:
   ```bash
   python app.py
   ```

### Production Deployment

#### General Instructions

1. Set up your server environment
2. Clone the repository
3. Install dependencies: `pip install -r requirements.txt`
4. Create a `.env` file with production settings
5. Use a WSGI server (Gunicorn, uWSGI) to run the application
   ```bash
   gunicorn wsgi:app
   ```

#### Platform-Specific Instructions

##### Heroku
```bash
heroku create
git push heroku main
heroku config:set SECRET_KEY=your_secret_key_here
```

##### PythonAnywhere
1. Clone the repo in your PythonAnywhere account
2. Create a virtual environment and install requirements
3. Set up a web app with the WSGI path pointing to `wsgi.py`

## Database

The application uses SQLite by default. For production, consider using a more robust database like PostgreSQL by updating the DATABASE_URL in your environment variables.