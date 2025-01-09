# to_do
updated to work with sqlalchemy


# Flask Todo Application

A simple Todo application built with Flask and SQLAlchemy that allows users to create, read, update, and delete todo items.

## Features

- Create new todos with title, description, and due date
- Mark todos as complete/incomplete
- Delete existing todos
- View all todos with their creation and due dates
- Responsive Bootstrap UI

## Technology Stack

- Python 3.x
- Flask
- SQLAlchemy (ORM)
- Bootstrap 5
- SQLite (Database)

## SQLAlchemy vs Raw SQLite

This application uses SQLAlchemy ORM (Object-Relational Mapping) instead of raw SQLite queries, providing several advantages:

- **Object-Oriented Approach**: Data is handled through Python classes instead of raw SQL queries
- **Database Agnostic**: Can easily switch to other databases (MySQL, PostgreSQL) by changing the connection string
- **Automatic Schema Management**: Models define the database structure in Python code
- **Query Abstraction**: Uses Python methods instead of writing raw SQL
- **Better Security**: Helps prevent SQL injection through parameter binding

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd todo-app
```

2. Create a virtual environment and activate it:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install required packages:
```bash
pip install flask flask-sqlalchemy
```

## Project Structure

```
todo_app/
    ├── app.py              # Main application file
    ├── todo.db            # SQLite database (created automatically)
    └── templates/         # HTML templates
        └── index.html     # Main page template
```

## Usage

1. Run the application:
```bash
python app.py
```

2. Open a web browser and navigate to:
```
http://localhost:5000
```

## Database Configuration

The application uses SQLAlchemy with SQLite by default. The database URI is configured in `app.py`:

```python
app.config['SQLALCHEMY_DATABASE_URI'] = 'sqlite:///' + os.path.join(basedir, 'todo.db')
```

To use a different database:
1. Install required driver (e.g., `psycopg2` for PostgreSQL)
2. Update the database URI:
   - PostgreSQL: `postgresql://username:password@localhost:5432/dbname`
   - MySQL: `mysql://username:password@localhost/dbname`

## Contributing

1. Fork the repository
2. Create a new branch
3. Make your changes
4. Submit a pull request

## License

This project is licensed under the MIT License - see the LICENSE file for details.
