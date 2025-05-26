# CSE-3107-Website
CSE 3107 Website

This repository contains a simple website for the CSE 3107: Computer Architecture (20 Series) course, inspired by Stanford's CS143 website. The website serves as a centralized hub for course materials, including lecture topics, resources, assignments, and handouts.

Project Overview

The website is built using Django with a single homepage that provides:





Course Overview: Introduction and lecture timing (TBD).



Resources: Links to textbooks, slides, and the HDL code repository.



Lectures: A list of lecture topics based on the syllabus.



Assignments: Placeholder links for programming and written assignments.



Handouts: Links to solutions (e.g., CT4 pipelining diagram problem).



More Information: Placeholder links to syllabus, discussion board, and grading rubrics.

The site uses plain HTML and CSS for simplicity, avoiding external dependencies like Tailwind CSS or JavaScript frameworks.

Requirements





Python 3.8+



Django 5.2.1



Gunicorn (for production deployment)



django-heroku (for Heroku deployment)

Setup Instructions





Clone the Repository:

git clone https://github.com/takitamim/CSE-3107-Website.git
cd CSE-3107-Website



Install Dependencies:

pip install -r requirements.txt



Apply Migrations:

python manage.py migrate



Run the Development Server:

python manage.py runserver

Open http://127.0.0.1:8000/ in your browser to view the website.

Project Structure





core/: Django app containing views, templates, and static files.





templates/core/home.html: Main homepage template.



static/css/style.css: Custom CSS for styling.



cse3107_website/: Django project settings and URL configurations.



requirements.txt: List of Python dependencies.



Procfile: Configuration for Heroku deployment.

Deployment on Heroku

The website is deployed on Heroku for free hosting. Follow these steps to deploy:





Install Heroku CLI: Download and install from Heroku CLI.



Log in to Heroku:

heroku login



Create a Heroku App:

heroku create cse3107-website



Add Heroku Remote:

heroku git:remote -a cse3107-website



Push to Heroku:

git push heroku main



Collect Static Files:

heroku run python manage.py collectstatic --noinput



Scale the Dyno:

heroku ps:scale web=1



Open the App:

heroku open

The app will be live at a URL like https://cse3107-website-123.herokuapp.com.
