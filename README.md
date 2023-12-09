# Vendor-Management-System

The Vendor Management System, developed using Django, is a web application designed for streamlined vendor relationship management.

It encompasses functionalities for managing vendor profiles, tracking purchase orders, and evaluating vendor performance.

Users can create, update, and delete vendor profiles, monitor purchase orders, and assess vendor performance metrics such as on-time delivery rate, quality rating average, average response time, and fulfillment rate.

# Tech Stack

Stack: Python, Django, dbsqlite3

Server: localhost:8000

# Installation

python -m venv venv

source venv/Scripts/activate

pip install django

pip install djangorestframework

pip install -r requirements.txt

python manage.py makemigrations 

python manage.py migrate

python manage.py createsuperuser 

python manage.py runserver

http://localhost:8000/admin  --for admin

# Deployment

 ($ pip freeze > requirements.txt)  ### It will freeze all the requirements in one txt file ###

 ($ git init)   ### It will initialize the folder as a local Git repository ###

 ($ git status)   ### This command to check if there are any changes to your Django code that need to be pushed to git ###

 ($ git add -A)   ### The -A flag is for all. It is used for adding all the commits to a repository ###

 ($ git commit -m "initial commit") ### It is for passing the message to repository ###

  ### Create A New Github Repository ###
  - Click the ‘+’ dropdown at the top right corner of your GitHub dashboard and click on the ‘New Repository’ option.
  - Type the name of the Repository. It is best practice to give it the same name as that of your Django project.
  - Give a description of the project if you wish to do so.
  - Choose if it is going to be a Private or Public directory.
  - The next step ‘Initialize your project with:’ is optional, skip it if you wish to.
  ### Click the ‘Create Reposity’ button ###

 ($ git remote add origin https://github.com/tinyjock/vendor-management-System.git)  ### It will add a new remote origin ###

 ($ git branch -M main)  ### It is used to shift to the main branch from master ###

 ($ git push -u origin main)  ### It will push your code the remote repository which you have added recently ###

# Instruction

1.Clone the Repository
git clone https://github.com/tinyjock/Vendor-Management-System.git

Install Dependencies: 
2.pip install -r requirements.txt 
3.Apply Migrations: python manage.py makemigrations and python manage.py migrate
4.Create Superuser: python manage.py createsuperuser 
5.Run Development Server: python manage.py runserver 
Access Admin Panel:

Visit http://127.0.0.1:8000/admin/ and log in with the superuser credentials.

Obtain Token:

Create a token for the superuser in the Django admin panel (/admin/authtoken/token/). Use this token for API authentication.

API Endpoints Vendor Management List/Create Vendors:

Endpoint: /api/vendors/ Method: GET (List all vendors) / POST (Create a new vendor) Retrieve/Update/Delete Vendor:

Endpoint: /api/vendors/{vendor_id}/ Method: GET (Retrieve) / PUT (Update) / DELETE (Delete) Vendor Performance Metrics:

Endpoint: /api/vendors/{vendor_id}/performance/ Method: GET Purchase Order Tracking List/Create Purchase Orders:

Endpoint: /api/purchase_orders/ Method: GET (List all purchase orders) / POST (Create a new purchase order) Retrieve/Update/Delete Purchase Order:

Endpoint: /api/purchase_orders/{po_id}/ Method: GET (Retrieve) / PUT (Update) / DELETE (Delete) Acknowledge Purchase Order:

Endpoint: /api/purchase_orders/{po_id}/acknowledge/ Method: POST

Token Authentication To access secured endpoints, include the token in the Authorization header: Authorization: Token your-token-here

Test Suite A comprehensive test suite is available in the tests directory. Run tests using: python manage.py test
