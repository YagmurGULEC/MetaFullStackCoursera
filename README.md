## How to Use
This is the repo as the capstone project in Meta Full Stack course on Coursera. 
I adapted this to run this on Docker instead of pipenv. It creates two containers, one of which is for the web application. The other is for mySQL. You can run this with the command below:

```
docker compose up --build
```
However to create the tables and you can give the connection error to the database. First you need to run migrations so that Django will create the tables.

```
docker compose exec web python manage.py makemigrations
docker compose exec web python manage.py migrate
```
You can list the tables with user booking_user by running the command below in the container db:
```
docker compose exec db mysql -u booking_user -p
```
and then enter the password:
```
booking_pass
```
You can use the command line:
```
USE booking_db;
SHOW TABLES;
SELECT * FROM restaurant_booking;
```





