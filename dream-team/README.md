### Getting Started

- Install dependencies

```bash
pip install virtualenv \
  Flask==0.12.2 flask-sqlalchemy Flask-WTF \
  flask-login flask-migrate flask-bootstrap\
  mysql-python \
  --user
```

- Prepare database

```bash
$ mysql -u root

mysql> CREATE USER 'dt_admin'@'localhost' IDENTIFIED BY 'dt2016';
Query OK, 0 rows affected (0.00 sec)

mysql> CREATE DATABASE dreamteam_db;
Query OK, 1 row affected (0.00 sec)

mysql> GRANT ALL PRIVILEGES ON dreamteam_db . * TO 'dt_admin'@'localhost';
Query OK, 0 rows affected (0.00 sec)
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