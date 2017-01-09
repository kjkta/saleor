# SETUP

Create virtualenv 
`virtualenv -p python3.5 env`

Install requirements 
`pip3 install -r requirements.txt`
`npm i`

Setup DB
Open postgress
`psql`
Create DB and User
```
CREATE USER saleor WITH PASSWORD 'saleor';  
ALTER ROLE saleor SUPERUSER;  
create database saleor;
GRANT ALL PRIVILEGES ON DATABASE saleor TO saleor;
```

Migrate DB
`./manage.py migrate`

Run the server
`./manage.py runserver`