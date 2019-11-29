# API Handler

________________________________________________________________________________________________________________________________________

# DESCRIPTION

Create a RESTful API to implement CRUD operations on data sent by http request. 

I chose to use this framework since it is scalable and functional.  The http requests are routed by Flask and SQLAlchemy interacts with the PSQL database to control the CRUD operations.  The JSON returned is serialized data from the PSQL db.

# LOCATION

IP address = localhost:5000

URL = http://localhost:5000/v1/

# SOFTWARE (Linux)

--Python--

1. Python 2.7 (apt-get install python2.7) **NOTE Python 2.7 libraries will be depreciated on 1/2020
2. Flask (pip install flask)
3. SQL Alchemy (pip install sqlalchemy)
4. Requests (pip install requests)
5. Psycopg2 (pip install psycopg2) + (pip install psycopg2-binary)

--Database--

Postgresql (sudo apt-get install postgresql-12)

SCRIPTS to run:

1. CREATE USER products_user WITH PASSWORD 'U$er';
2. CREATE TABLE products (id serial, Name varchar(250), Price varchar(250));
3. GRANT ALL PRIVILEGES ON products TO products_user;
4. GRANT USAGE, SELECT ON SEQUENCE products_id_seq TO products_user;

# TO RUN PROGRAM

1. Download and install software (Outlined above)
2. Start PostgreSQL server (pg_ctlcluster 12 main start)
3. Run PSQL scripts as POSTGRES user (-u postgres -i)
4. Clone repository https://github.com/NSPurington/API_Test_Handler (git clone ....)
5. Run add_products.py (python add_products.py)
6. Run __init__.py (python __init__.py) (Include 2 underscores before and after 'init'.  Escaped out in GitHub formatting)
7. Send API calls to http://localhost:5000/v1/ (using Postman or Curl)

# LANGUAGES

This app is programmed with Python back-end code, and uses Flask, SQL Alchemy, and Psycopg2 to interact with non-Python sources.


# AKNOWLEDGEMENTS

 Flask documentation - Online
 SQL Alchemy documentation - Online
 Postgresql official documentation - Online
 Psycopg2 official documentation - Online

Author - Nick Purington - Developer
