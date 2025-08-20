## PIZZA DELIVERY API
This is a REST API for a Pizza delivery service built for fun and learning with FastAPI, SQLAlchemy and PostgreSQL.


## ROUTES TO IMPLEMENT
| METHOD | ROUTE | FUNCTIONALITY |ACCESS|
| ------- | ----- | ------------- | ------------- |
| *POST* | ```/auth/signup/``` | _Register new user_| _All users_|
| *POST* | ```/auth/login/``` | _Login user_|_All users_|
| *POST* | ```/orders/order/``` | _Place an order_|_All users_|
| *PUT* | ```/orders/order/update/{order_id}/``` | _Update an order_|_All users_|
| *PUT* | ```/orders/order/status/{order_id}/``` | _Update order status_|_Superuser_|
| *DELETE* | ```/orders/order/delete/{order_id}/``` | _Delete/Remove an order_ |_All users_|
| *GET* | ```/orders/user/orders/``` | _Get user's orders_|_All users_|
| *GET* | ```/orders/orders/``` | _List all orders made_|_Superuser_|
| *GET* | ```/orders/orders/{order_id}/``` | _Retrieve an order_|_Superuser_|
| *GET* | ```/orders/user/order/{order_id}/``` | _Get user's specific order_|
| *GET* | ```/docs/``` | _View API documentation_|_All users_|

## How to run the Project
- Install Postgreql
- Install Python
- Git clone the project with ``` git clone https://github.com/kuchurisatwik/Pizza-Delivery-API.git```
- Create your virtualenv with `Pipenv` or `virtualenv` and activate it.
- Install the requirements with ``` pip install -r requirements.txt ```
- Set Up your PostgreSQL database and set its URI in your ```database.py```
```
engine=create_engine('postgresql://postgres:<username>:<password>@localhost/<db_name>',
    echo=True
)
```

- Create your database by running ``` python init_db.py ```
- Finally run the API
``` uvicorn main:app ``

## Lessons I learned

- I learned how APIs work from building the endpoints — for example, /orders/order/ taught me how to send and receive JSON using HTTP methods.

- I learned user auth and security from the signup/login flow — hashing passwords and protecting routes showed me why authentication matters.

- I learned databases and ORM from using SQLAlchemy and Postgres — modelling tables as classes and using sessions made data handling easier.

- I learned project setup & running basics from using virtualenv and running the app with uvicorn — it taught me how to prepare the project so others can run it.


