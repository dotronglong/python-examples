### Getting Started

- Install dependencies

```bash
pip install virtualenv \
  Flask==0.12.2 flask-sqlalchemy Flask-WTF \
  flask-login flask-migrate flask-bootstrap\
  mysql-python \
  --user
```

- Run database migrations

```bash
flask db init
flask db migrate
```

- Start application

```bash
export FLASK_CONFIG=development
export FLASK_APP=run.py
flask run
```