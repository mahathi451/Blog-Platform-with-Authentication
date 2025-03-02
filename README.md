# ✍️ Modern Blog Platform

![Flask](https://img.shields.io/badge/Framework-Flask-green)
![SQLAlchemy](https://img.shields.io/badge/ORM-SQLAlchemy-blue)
![Bootstrap](https://img.shields.io/badge/UI-Bootstrap-563D7C)

A full-featured blogging platform with secure authentication and content management.

## 🔑 Core Features

### 🔒 Security System
- Password hashing with bcrypt
- Session-based authentication
- CSRF protection
- Role-based access control

### 📝 Content Management
- Rich text editor (Markdown support)
- Post scheduling
- Draft management
- SEO-friendly URLs

## 🛠 Tech Stack

Component | Technology
---|---
Frontend | Jinja2, Bootstrap 5
Backend | Flask
Database | SQLAlchemy (SQLite/PostgreSQL)
Auth | Flask-Login, Flask-WTF

## 🚀 Quick Start

git clone https://github.com/yourusername/blog-platform.git
cd blog-platform
Set up environment

python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
Initialize database

flask db init
flask db migrate
flask db upgrade
Run application

flask run
text

## 📚 API Endpoints

Method | Endpoint | Description
---|---|---
GET | /api/posts | List all posts
POST | /api/posts | Create new post
PUT | /api/posts/<id> | Update post
DELETE | /api/posts/<id> | Delete post

## 🧩 Database Schema

class User(db.Model):
id = db.Column(db.Integer, primary_key=True)
username = db.Column(db.String(20), unique=True)
email = db.Column(db.String(120), unique=True)
password_hash = db.Column(db.String(128))
class Post(db.Model):
id = db.Column(db.Integer, primary_key=True)
title = db.Column(db.String(100))
content = db.Column(db.Text)
user_id = db.Column(db.Integer, db.ForeignKey('user.id'))
