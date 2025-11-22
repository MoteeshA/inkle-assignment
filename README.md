
---

## **README.txt**

Inkle Mini Twitter – Backend API (Flask + JWT)

A lightweight backend that implements core Twitter-like features including user authentication, posting, following, blocking, liking, unliking, and activity feed. All endpoints are tested using Postman.

---

## FEATURES IMPLEMENTED

Authentication

* User Signup
* User Login
* JWT Token-based Authentication

Posts

* Create Post
* Get All Posts
* Like Post
* Unlike Post

User Interactions

* Follow User
* Unfollow User
* Block User

Activity Feed

* View activity of user + following
  (Posts, likes, follows, blocks in chronological order)

Postman

* All endpoints tested
* Postman collection exported

---

## TECH STACK

* Python 3
* Flask
* Flask SQLAlchemy
* Flask-JWT-Extended
* Flask-CORS
* SQLite (default)
* Postman

---

## PROJECT STRUCTURE

mini-twitter-backend/
app.py
config.py
models.py
auth_routes.py
user_routes.py
post_routes.py
activity_routes.py
requirements.txt
README.md
instance/
database.sqlite  (auto-created)

---

## INSTALLATION AND SETUP

1. Clone the repository:
   git clone <your-repo-url>
   cd mini-twitter-backend

2. Create virtual environment:
   python3 -m venv venv
   source venv/bin/activate

3. Install dependencies:
   pip install -r requirements.txt

4. Run the application:
   python app.py

Server runs at:
[http://127.0.0.1:5000](http://127.0.0.1:5000)

---

## AUTHENTICATION

Login returns a JWT token like this:

{
"access_token": "<JWT_TOKEN>",
"user": { ... }
}

Use this in Postman:
Authorization -> Bearer Token -> paste token

---

## API ENDPOINTS

AUTH
POST /auth/signup      - Register new user
POST /auth/login       - Login and get token

POSTS
POST /posts/           - Create post
GET  /posts/           - Get all posts
POST /posts/<id>/like  - Like post
POST /posts/<id>/unlike - Unlike post

USERS
POST /users/follow/<id>     - Follow user
POST /users/unfollow/<id>   - Unfollow user
POST /users/block/<id>      - Block user

ACTIVITY
GET /activity/         - Get activity feed

---

## POSTMAN COLLECTION

Includes:

* Sign Up
* Login
* Create Post
* Get Posts
* Follow
* Unfollow
* Block
* Like
* Unlike
* Activity Feed

Export from Postman:
Collections → ... → Export

---

## NOTES

* SQLite DB creates automatically.
* Token expiry can be modified in config.py.
* Authorization header is required for all protected routes.

---

## REQUIREMENTS.TXT

Flask
Flask-SQLAlchemy
Flask-JWT-Extended
Flask-CORS
Werkzeug

---

## FINAL OUTPUT INCLUDES

* Complete backend API
* All endpoints working
* Postman tested
* README documentation
* Ready for submission

---

