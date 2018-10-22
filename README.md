# Uptrend

Automated remote deploy of app + clusters:

```
pip install cookiecutter
```
Open a new tab in command line and type:
```
openssl rand -hex 32
# Outputs something like: 99d3b1f01aa639e4a76f4fc281fc834747a543720ba4c8a8648ba755aef9be7f

cookiecutter pip install cookiecutter
cookiecutter https://github.com/joehoeller/uptrend
```
Follow the prompts until you get to: ```secret_key [changethis]:``` Go to the next tab and copy/paste 
the openssl key in to encrypt the app cluster.

Then cd /"project_name" folder, and run:
```
docker-compose build
```
And then start the machine learning infrastructure:
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

