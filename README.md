# Rooms Manager
This is an Spring Boot API to manage meeting rooms. For data persistence we choosed Spring Data and in-memory database H2. The frontend was developed as an Angular SPA.

We configure a small microservices architeture to run the services (backend and frontend) independently, with Docker.

## Running this application

### Requirements
You only need Docker to run this application.

### Running
After downloading and extracting the code, enter the folder and run the commands:

`docker compose build`
This will take some time.

`docker compose up`

### Accessing
Open your browser and navigate to [localhost](http://localhost).

Note that we are using ports 80 for frontend and 8082 to backend.

#### This application is for studying purposes only.

