# Lab 1: Setup and Containerize Moments

## Goal
Setup the Moments web application, and containerize the application using Docker.

## Prerequisites
- Python 3.10, pip
- Basic Git usage
- Docker installed
- Clone of the [Moments project](https://github.com/greyli/moments) (or your fork)

---

## Part 1: Set Up Moments Locally

```bash
# Clone Moments and cd into the repository
git clone https://github.com/greyli/moments
cd moments

# Create and activate virtual environment
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows

# Install dependencies
pip install -r requirements.txt

# Initialize app
flask init-app

# Generate fake data for testing
flask lorem

# Run the app
flask run
```

You should see Moments running at http://127.0.0.1:5000

---

## Part 2: Dockerize the App

### Add Dockerfile:
```Dockerfile
# Dockerfile
FROM python:3.10-slim

WORKDIR /moments
COPY . /moments

RUN pip install --upgrade pip && \
    pip install -r requirements.txt

ENV FLASK_APP=app.py
ENV FLASK_ENV=dev

# Initialize app and populate fake data
RUN flask init-app && flask lorem

CMD ["flask", "run", "--host=0.0.0.0"]
```

### Build and Run:
```bash
docker build -t moments .
docker run -p 5000:5000 moments
```
