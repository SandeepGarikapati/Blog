# Flask Blog Website

This is a Flask-based blog website where users can register, log in, create, and view blog posts. Admin users have additional permissions to manage (add, edit, delete) posts and comments. The website also includes features like user authentication, commenting, and contact forms.

## Features

- **User Authentication:**
  - Register new users
  - Log in and log out users
  - Password hashing for secure authentication
  - Forgot and reset password functionality

- **Blog Post Management:**
  - Users can view blog posts
  - Admin users can create, edit, and delete posts
  - Admin users can also manage comments

- **Commenting:**
  - Logged-in users can comment on posts
  - Comments are associated with users and posts

- **Contact Form:**
  - A contact form that sends messages via email using SMTP

- **Profile Images:**
  - User profile images are generated using Gravatar

## Technologies Used

- **Flask:** Web framework
- **Flask-Login:** User authentication and session management
- **Flask-WTF:** Form handling
- **Flask-Bootstrap:** Frontend framework for styling
- **Flask-Gravatar:** For profile images
- **SQLAlchemy:** ORM for database interactions
- **Jinja2:** Templating engine
- **SMTP:** For email sending via Gmail
- **HTML/CSS:** Frontend design

## Prerequisites

- Python 3.x
- Flask and other required packages (install using `requirements.txt`)

## Installation

1. Clone this repository:

   ```bash
   git clone https://github.com/your-username/flask-blog-website.git
   cd flask-blog-website
   ```
2. Install the required Python packages
   ```bash
   pip install -r requirements.txt
   ```
3.Intiliaze the DB
  ```bash
  app.config['SQLALCHEMY_DATABASE_URI'] = os.environ.get("DB_URI", "sqlite:///posts.db")
  ```
4. Run the flask application
   ```bash
   flask run
   ```

## Usage
- Visit the home page to view all blog posts.
- Register a new account or log in if you already have one.
- Admin users can create, edit, and delete posts.
- Logged-in users can comment on posts.
- Use the contact form to send messages to the admin.

## Admin Access
- To access the admin features, the first registered user (with ID 1) has admin privileges by default. You can update this in the code if needed.

## SMTP Configuration
- To enable the contact form, you need to set up SMTP for email sending. Ensure that you have enabled "Less secure apps" or use an app-specific password for Gmail.
```bash
  EMAIL = "your-email@gmail.com"
  PASS = os.environ.get('PASS')  # Your Google App Password
```

## Acknowledements
- Flask documentation
- Bootstrap for styling
- Gravatar for profile images

 
