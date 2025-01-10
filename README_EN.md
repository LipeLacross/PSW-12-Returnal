## 🌐 [English Version of README](README_EN.md)

# PSW 12 RETURNAL

This repository contains three distinct projects: one for URL shortening management, one for creating a digital diary, and one for data monitoring. Each project has its own functionality and structure, and the following documentation explains how to set up and run each of them.

---

## 🟠 Project 1: URL Shortener

This project is a simple URL shortener developed with Django and the NinjaAPI library. It allows users to create shortened links, track unique clicks, and manage links with an expiration time. The main goal is to facilitate the creation of short links that redirect users to original URLs, with the ability to limit the number of clicks and set an expiration time.

### 🔨 Features

- Create shortened links from provided URLs.
- Control expiration and limit unique clicks.
- API for creating and managing links.

### ✔️ Techniques and Technologies

- **Django** for backend.
- **NinjaAPI** for creating API endpoints.
- **TailwindCSS** for styling.
- **SQLite** as the database.

### 📁 Project Structure

- **core/**
    - `settings.py`, `urls.py`, `wsgi.py`, `asgi.py`
- **shortener/**
    - `models.py`, `api.py`, `schemas.py`, `views.py`, `admin.py`
    - `migrations/`: Database migration files.
- **manage.py**: Django management script.

### 🛠️ Running the Project

1. **Install dependencies**:
    - Run `pip install -r requirements.txt`.
2. **Run migrations**:
    - Run `python manage.py migrate`.
3. **Start the Django server**:
    - Run `python manage.py runserver`.

---

## 🟢 Project 2: Digital Diary

This project is a digital diary where you can log and view personal entries. It uses Django for the backend and TailwindCSS for the frontend. The system allows the user to record entries with information such as title, content, and date.

### 🔨 Features

- Record diary entries with title, content, and date.
- View recorded entries.
- Simple and intuitive interface.

### ✔️ Techniques and Technologies

- **Django** for backend.
- **TailwindCSS** for responsive design.
- **SQLite** for storing entries.

### 📁 Project Structure

- **core/**
    - `settings.py`, `urls.py`, `wsgi.py`, `asgi.py`
- **diary/**
    - `models.py`: Contains the data model for diary entries.
    - `views.py`: Defines the views to display the diary.
    - `templates/`: Contains the HTML to display the entries.
- **manage.py**: Django management script.

### 🛠️ Running the Project

1. **Install dependencies**:
    - Run `pip install -r requirements.txt`.
2. **Run migrations**:
    - Run `python manage.py migrate`.
3. **Start the Django server**:
    - Run `python manage.py runserver`.

---

## 🔵 Project 3: Data Monitoring

This project is a data monitoring system using Flask, SQLite, and real-time charts with Chart.js. The goal is to collect sensor data and present it in interactive graphs in real-time.

### 🔨 Features

- Collect sensor data via POST.
- Visualize real-time charts using Chart.js.
- Export data to CSV.

### ✔️ Techniques and Technologies

- **Flask** for backend.
- **Chart.js** for data visualization.
- **SQLite** for storing data.

### 📁 Project Structure

- **core/**
    - `app.py`: Main file that initializes the Flask server and routes.
    - `models.py`: Defines the data model for storing sensor readings.
    - `static/`: Contains static files like images and charts.
    - `templates/`: Contains HTML templates to display data.
- **requirements.txt**: List of project dependencies.
- **manage.py**: Management script for running the Flask server.

### 🛠️ Running the Project

1. **Install dependencies**:
    - Run `pip install -r requirements.txt`.
2. **Start the Flask server**:
    - Run `python app.py`.
3. **Access the system**:
    - Open your browser and visit `http://127.0.0.1:5000/` to view the data monitoring system in action.

---

## 🌐 Deploy

To deploy any of the projects, follow these steps:

1. **Configure the Database**:
    - For production environments, set up a database like PostgreSQL.
2. **Configure the Server**:
    - Use a deployment service like [Heroku](https://www.heroku.com/) or [DigitalOcean](https://www.digitalocean.com/).
3. **Deploy the Project**:
    - For Heroku, you can follow the [Django deployment documentation](https://devcenter.heroku.com/articles/django-app-configuration) or [Flask](https://devcenter.heroku.com/articles/getting-started-with-python).
4. **Access the Project**:
    - After deployment, you can access the application through the domain provided by the hosting platform.
