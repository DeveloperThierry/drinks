# Drinks API

A RESTful API application built with Django and Django REST Framework to manage a collection of beverages. This project demonstrates the fundamentals of building a robust API, including model creation, serialization, view configuration, and CRUD operations.

## Project Overview

The Drinks API allows users to interact with beverage data programmatically. It supports standard HTTP methods (GET, POST, PUT, DELETE) and is configured to handle data formats in both HTML (browsable API) and JSON.

## Prerequisites

*   Python 3.x
*   pip (Python package manager)
*   Virtual environment tool (venv)

## Getting Started

### Installation

1.  Create and activate a virtual environment:

    ```bash
    python3 -m venv .venv
    source .venv/bin/activate
    ```

2.  Install the required dependencies:

    ```bash
    pip install -r requirements.txt
    ```

3.  Initialize the database by applying migrations:

    ```bash
    python manage.py migrate
    ```

4.  Create an administrative user to manage data via the Django admin interface:

    ```bash
    python manage.py createsuperuser
    ```

### Running the Application

Start the development server:

```bash
python manage.py runserver
```

The API will be available at `http://127.0.0.1:8000/`.

## API Endpoints

*   `GET /drinks/`: Retrieve a list of all available drinks.
*   `POST /drinks/`: Create a new drink entry.
*   `GET /drinks/<id>/`: Retrieve details for a specific drink by its ID.
*   `PUT /drinks/<id>/`: Update an existing drink entry.
*   `DELETE /drinks/<id>/`: Remove a drink from the database.

## Usage Example

To consume the API using Python's `requests` library:

```python
import requests

response = requests.get('http://127.0.0.1:8000/drinks/')
print(response.json())
```

## License
The MIT License (MIT)

Copyright (c) 2026 Thierry

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
