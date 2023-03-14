Django Vue Docker Project Template
==================================

This is a template project for building a web application using Django, Vue.js and Docker.

Prerequisites
-------------

Before starting, you should have the following software installed on your machine:

*   [Docker](https://www.docker.com/)
*   [Docker Compose](https://docs.docker.com/compose/)

Moreover it has preinstalled some standard Django and Vue libraries for build web applications.
Getting Started
---------------

To get started, clone this repository to your local machine:
```bash
git clone https://github.com/yourusername/django-vue-docker-project-template.git 
cd django-vue-docker-project-template
```
and build the images
```bash
docker-compose build
```

### Setting up the Backend

To set up the Django backend, navigate to the `backend` directory and run the following commands:

```bash
docker-compose run backend python manage.py migrate 
docker-compose run backend python manage.py createsuperuser
docker-compose up -d 
```

These commands will start the Docker containers, run the necessary database migrations, and create a superuser for the Django admin interface.

### Setting up the Frontend

To set up the Vue.js frontend, navigate to the `frontend` directory and run the following commands:

```bash
npm run serve
```

This command start the development server.

### Accessing the Application

You can access the application by navigating to [http://localhost:8080](http://localhost:8080) in your web browser. You should see a default Vue.js application running.

To access the Django admin interface, navigate to [http://localhost:8000/admin](http://localhost:8000/admin) and log in using the superuser credentials you created earlier.

License
-------

This project is licensed under the MIT License - see the [LICENSE](LICENCE) file for details.