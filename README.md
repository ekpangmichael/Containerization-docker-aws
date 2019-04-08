# containerization

I deployed a micro service architecture on GCP using Docker

# How it works
- I created a kubernetes cluster on GCP
- Then i created different workloads for deployments 
The application has a frontend, catalogue, catalogue_db and cart service
- I created a loadbalancer that receives traffic from the internet into the nodes
- I created the cluster ip that enables the containers to communicate

# How application containerization works
Application containers include the runtime components -- such as files, environment variables and libraries -- necessary to run the desired software. Application containers consume fewer resources than a comparable deployment on virtual machines because containers share resources without a full operating system to underpin each app. The complete set of information to execute in a container is the image. The container engine deploys these images on hosts.
