# Microblog

Microblog is a simple Flask-based web application that mimics the basic functionality of a blogging platform.

## Features

- User registration and authentication
- User profile pages
- Blogging functionality (creating, editing, and deleting posts)
- Following and unfollowing users
- Timeline of posts from followed users
- Pagination
- Password hashing and secure login
- Email notifications for password recovery
- Full-text search using Elasticsearch
- API for mobile or third-party integrations
- Internationalization support with translations

## Installation

To install and run the project locally, follow these steps:

### Prerequisites

- Python 3.7+
- [Flask](https://flask.palletsprojects.com/)
- [Elasticsearch](https://www.elastic.co/elasticsearch/) (for full-text search, optional)
- A database such as SQLite or PostgreSQL

### Steps

1. Clone the repository:

    ```bash
    git clone https://github.com/miguelgrinberg/microblog.git
    cd microblog
    ```

2. Set up a virtual environment (optional but recommended):

    ```bash
    python3 -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    ```

3. Install dependencies:

    ```bash
    pip install -r requirements.txt
    ```

4. Set up the environment variables:

    ```bash
    export FLASK_APP=microblog.py
    export FLASK_ENV=development  # Enables debug mode
    ```

5. Initialize the database:

    ```bash
    flask db upgrade
    ```

6. (Optional) Set up Elasticsearch if you want full-text search functionality:

    - Install and start Elasticsearch.
    - Update `config.py` to include your Elasticsearch URL.

7. Run the application:

    ```bash
    flask run
    ```

    Visit `http://localhost:5000` in your web browser to access the application.

## Usage

### Creating a User

To create an account, go to the "Register" page and fill out the registration form. You can then log in using your credentials.

### Posting

Once logged in, you can write new blog posts, edit existing ones, or delete them. You can also follow other users and see their posts on your personalized timeline.

### API Access

The project includes an API that allows third-party applications to interact with the platform. You can use the API to create, retrieve, update, and delete posts.

## Testing

To run the tests, execute:

```bash
flask test
