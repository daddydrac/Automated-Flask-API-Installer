# Automated Flask API Installer
Automated login/auth, database deployemnt with PostgresSQL and PGADMIN, with a fully functional front end in VueJS -- sets up all in the command line in seconds!

Automated remote deploy of app + clusters:

```
pip install cookiecutter
```
Open a new tab in command line and type:
```
openssl rand -hex 32
# Outputs something like: 99d3b1f01aa639e4a76f4fc281fc834747a543720ba4c8a8648ba755aef9be7f

cookiecutter git@github.com:joehoeller/Automated-Flask-API-Installer.git
```
Follow the prompts until you get to: ```secret_key [changethis]:``` Go to the next tab and copy/paste 
the openssl key in to encrypt the app cluster.

For the Sentry.io prompt add:
```
https://01a48442768f414dae1094221e5e6a9c@sentry.io/1305465
```
To add Sentry to your Python code, simply write:
```
$ pip install --upgrade sentry-sdk==0.4.3

import sentry_sdk
sentry_sdk.init("https://01a48442768f414dae1094221e5e6a9c@sentry.io/1305465")
```

Then cd /"project_name" folder, and run:
```
docker-compose build
```
And then start the GUI and backend infrasturcture to support your machine learning app:
```
docker-compose up -d
```

Now you can open your browser and interact with these URLs: 

-Frontend, built with Docker, with routes handled based on the path: http://localhost
 
-Backend, JSON based web API, with Swagger automatic documentation: http://localhost/api/ 

-Swagger UI, frontend user interface to interact with the API live: http://localhost/swagger/ 

-PGAdmin, PostgreSQL database web administration: http://localhost:5050 

-Flower, administration of Celery tasks: http://localhost:5555 

-Traefik UI, to see how the routes are being handled by the proxy: http://localhost:8090

----------------------------------------------------------------------------------------

### Credits

Based on the work of Sebastián Ramírez: https://github.com/tiangolo/full-stack-fastapi-couchbase
