

## What is containerization

Containerization is the process of encapsulating your application into a container.

It involves bundling an application together with all of its related configuration files, libraries and dependencies required for it to run in an efficient and bug-free way across different computing environments.

In the areas of software development, containerization is the encapsulation of an application with its own operating environment which can be run on any host machine without installing any more dependencies. It is a uniform structure in which an application can be stored.

The most popular containerization ecosystems are Docker and Kubernetes.

**What is Docker**

Docker is a tool that makes it easier to create, deploy, and run any applications by using containers. Containers allow a developer to package up an application with all of the parts it needs, such as libraries and other dependencies, and ship it all out as one package.

**What is Kubernetes**

Kubernetes is an open source container orchestration system that is used to automate application deployment, scaling application and managing containers. It is also a platform for managing containerized workloads and service across a collection of cluster host.

At Travela we have different Docker files which we use to build the docker images that runs our application.
For development we have a docker that builds our frotend and backend images . 
For the backenmd, we use a docker compose file to run the application in developer. This docker compose file create two containers, one is the *app container* this runs the backend functionality of the application. Another one is the *Database container* This runs a postgres image which holds the apllication database.


#### Below are the docker files for our application
- https://drive.google.com/file/d/1hk60pj22ZAd9FNKLd3yOwGMguobhS-le/view?usp=sharing
- https://drive.google.com/file/d/1ncejisAq4GrphsmozoY6FAlQxRYMBOdX/view?usp=sharing


The frontend docker file also create the frontend container which holds the frontend functionalities

#### Image Link
- https://drive.google.com/file/d/14YisZgO35NZoftSBpzyrJS5WAZMidkt2/view?usp=sharing


## For Staging

In the staging environment, we have a CI/CD pipeline that deploys the application. The application is deployed when a new feature, bug or chore has been merged to develop branch, and this is deployed to GCP (Google Cloud platform).

For the deployment to occur all the required criteria must be met, example all the test must pass before that branch can be merged.

Before the app is deployed, the CI/CD platform will use the release docker file to build the image of our application, this image is then pushed to GCR (google container registry). The image is then used to deploy the application in the staging cluster.

#### Images
##### Circle CI workflow that deploys to staging.
1.[Frontend](https://drive.google.com/file/d/1vuseG_yInP8Y-EUwbgGsp5X_T_4q_aJz/view?usp=sharing)

2.[Backend](https://drive.google.com/file/d/1kcpYZoe-2_WQE6qrFm6pqwbux3Bt5zNG/view?usp=sharing)



## For production

For production, the application is deployed on travela-production cluster, both the frontend and backend container runs on this cluster.

#### Images
##### Circle CI workflow that deploys to production
1.[Frontend](https://drive.google.com/file/d/1PmaNn1E2_6ch8kB0AsOhuI6noPaI69x-/view?usp=sharing)

2.[Backend](https://drive.google.com/file/d/12Xq2fH_B3Q6T0aHnVADYodZy4CNSp97h/view?usp=sharing)



##### Images to circle CI configuration that helps with the deployment

1. Backend configuration:
- https://drive.google.com/file/d/1WKz5tIoGehUuQB5-U6AdnLUhWNnnP4ud/view?usp=sharing
- https://drive.google.com/file/d/1GYmLuy5gOy2EY9gnYI_ACql14fOQjpGT/view?usp=sharing



2. Frontend configuration
- https://drive.google.com/file/d/1Ovegz8tzNno8W3iAH1HU2kNp78Ty_39t/view?usp=sharing
- https://drive.google.com/file/d/1-KDhDEVx0fOBuYgSSMnd-cOCX4n7y9gF/view?usp=sharing

