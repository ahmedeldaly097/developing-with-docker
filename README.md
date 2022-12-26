## Developing with Docker

This app shows a simple user profile app set up using 
- index.html with pure js and css styles
- nodejs backend with express module
- mongodb for data storage
## Mode Demo

---
https://user-images.githubusercontent.com/111642557/204152576-24cc8aec-dc1a-47c6-839e-52e608a25b6f.mp4
---

## All components are docker-based

### With Docker Compose

#### To start the application
---
Step 1: Pull mongodb and mongo-express images on your machine.

    docker pull mongo
    docker pull mongo-express
---
Step 2: Build your Web_App using Dockerfile and give it a Tag.

    docker build -t my_web_app:1.0 .
    
The dot "." at the end of the command denotes location of the Dockerfile.
---
Step 3: Push the image to the AWS ECR.

    docker push <AWS ECR> 
--- 
Step 4: Run container images from mongodb, mongo-express and ECR images using docker-compose in detached mode.

    docker-compose -f docker-compose.yaml up -d
---
Step 5: access the mongo-express application from your browser.

    http://localhost:8081
---
Step 6: access the nodejs application from browser 

    http://localhost:3000
---
