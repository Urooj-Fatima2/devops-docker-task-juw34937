\# DevOps Docker Task



\## Student Information



\- \*\*Name:\*\* Hafiza Urooj Fatima

\- \*\*Student ID:\*\* juw34937

\- \*\*Course:\*\* DevOps



\## Application Description



A simple static web application built with HTML. The application displays the student's name, student ID, course name, and a message confirming that the application is running inside a Docker container.



The website is served using the official lightweight Nginx web server image.



\## Technologies Used



\- Git

\- GitHub

\- Docker

\- Docker Hub

\- HTML

\- Nginx



\## Dockerfile Explanation



The application is containerized using Nginx.



```dockerfile

FROM nginx:alpine



COPY index.html /usr/share/nginx/html/index.html



EXPOSE 80

```



\### Dockerfile Instructions



\- `FROM nginx:alpine` — uses the official lightweight Nginx image as the base image for serving the static web application.

\- `COPY index.html /usr/share/nginx/html/index.html` — copies the application's `index.html` file into the default Nginx web directory inside the container.

\- `EXPOSE 80` — documents port 80, which is the default port used by Nginx inside the container.



\## .dockerignore



The project also contains a `.dockerignore` file to prevent unnecessary files from being included in the Docker build context.



```text

.git

.gitignore

README.md

.env

npm-debug.log

node\_modules

```



\# Git and GitHub



\## Git Commands



The project was initialized and uploaded to GitHub using the following commands:



```bash

git init

git status

git add .

git commit -m "Initial Docker application"

git branch -M main

git remote add origin https://github.com/Urooj-Fatima2/devops-docker-task-juw34937.git

git push -u origin main

```



\## GitHub Repository



\*\*GitHub Repository:\*\*



https://github.com/Urooj-Fatima2/devops-docker-task-juw34937



\# Docker Commands



\## Build Docker Image



The Docker image was built using:



```bash

docker build -t devops-task:v1 .

```



\## Check Docker Images



```bash

docker images

```



The Docker image was successfully created with the name:



```text

devops-task:v1

```



\## Run Docker Container



```bash

docker run -d -p 3000:80 --name devops-task devops-task:v1

```



The `-p 3000:80` option maps port 3000 on the host computer to port 80 inside the Docker container.



Therefore, the application can be accessed through:



```text

http://localhost:3000

```



\## Check Running Containers



```bash

docker ps

```



\## View Container Logs



```bash

docker logs devops-task

```



\## Inspect Container



```bash

docker inspect devops-task

```



\# Docker Hub



\## Docker Login



```bash

docker login

```



\## Tag Docker Image



The Docker image was tagged using the Docker Hub username:



```bash

docker tag devops-task:v1 hafizauroojfatima/devops-task:v1

```



\## Push Image to Docker Hub



```bash

docker push hafizauroojfatima/devops-task:v1

```



The image was successfully pushed to Docker Hub with the `v1` tag.



\## Docker Hub Repository



https://hub.docker.com/repositories/hafizauroojfatima



\# Pull Image from Docker Hub



To verify that the image could be downloaded and used independently from the local Docker build, the image was pulled from Docker Hub.



```bash

docker pull hafizauroojfatima/devops-task:v1

```



The image was successfully pulled from Docker Hub.



\# Run the Pulled Image



The image pulled from Docker Hub was used to create a new Docker container:



```bash

docker run -d -p 3000:80 --name devops-task-pulled hafizauroojfatima/devops-task:v1

```



\## Verify Pulled Container



```bash

docker ps

```



\## View Pulled Container Logs



```bash

docker logs devops-task-pulled

```



\## Inspect Pulled Container



```bash

docker inspect devops-task-pulled

```



\# Application Verification



The application was successfully tested in the browser using:



```text

http://localhost:3000

```



The application successfully displayed while running inside the Docker container.



The application was also successfully verified after pulling the Docker image directly from Docker Hub and running the pulled image as a new container.



\# Complete Workflow



The complete workflow followed in this task was:



```text

Create Web Application

&#x20;       ↓

Initialize Git Repository

&#x20;       ↓

Push Project to GitHub

&#x20;       ↓

Create Dockerfile

&#x20;       ↓

Create .dockerignore

&#x20;       ↓

Build Docker Image

&#x20;       ↓

Run Docker Container

&#x20;       ↓

Verify Application

&#x20;       ↓

Tag Docker Image

&#x20;       ↓

Push Image to Docker Hub

&#x20;       ↓

Remove Local Container/Image

&#x20;       ↓

Pull Image from Docker Hub

&#x20;       ↓

Run Pulled Image

&#x20;       ↓

Verify Application Again

```



\# Screenshots



The following screenshots are included as evidence of the completed task:



1\. GitHub repository

2\. Dockerfile

3\. `.dockerignore`

4\. Docker image build

5\. `docker images`

6\. Running Docker container using `docker ps`

7\. Application running in the browser

8\. Docker Hub repository

9\. Docker image push

10\. Docker image pull

11\. Container running from the pulled Docker Hub image

12\. Final application verification after pulling the image



\# Repository Links



\## GitHub



https://github.com/Urooj-Fatima2/devops-docker-task-juw34937



\## Docker Hub



https://hub.docker.com/repositories/hafizauroojfatima



\## Application



http://localhost:3000



\# Conclusion



The web application was successfully version-controlled using Git and GitHub, containerized using Docker and Nginx, pushed to Docker Hub, pulled again from Docker Hub, and successfully executed inside a Docker container.



The final application was verified successfully through the browser at:



http://localhost:3000

