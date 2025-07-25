# Docker Foundations Quiz

## Question 1
**Which of the following best describes the role of the Docker Daemon?**

A. It builds Dockerfiles into containers  
B. It acts as a bridge between the container and host filesystem  
C. It listens to Docker API requests and manages Docker objects  
D. It controls the container's network settings only  

**Answer:** C

---

## Question 2  
**Which of the following best describes containerization compared to virtualization?**

A. Containerization uses more resources  
B. Containerization runs separate OS kernels for each app  
C. Containerization shares the host OS kernel  
D. Containerization is slower but more isolated  

**Answer:** C

---

## Question 3
**Which of the following is NOT a Linux namespace used in containerization?**

A. NET  
B. USER  
C. PROC  
D. PID  

**Answer:** C

---

## Question 4  
**What does the `FROM` instruction do in a Dockerfile?**

A. Runs a command inside the image  
B. Copies files into the container  
C. Specifies the base image to use  
D. Exposes a port  

**Answer:** C

---

## Question 5  
**Which command is used to build a Docker image from a Dockerfile?**

A. `docker run`  
B. `docker start`  
C. `docker build`  
D. `docker compose`  

**Answer:** C

---

## Question 6  
**Which of the following best describes a Docker image?**

A. A running instance of a container  
B. A snapshot of a container's logs  
C. A lightweight, read-only blueprint to create containers  
D. The network configuration for a container  

**Answer:** C

---

## Question 7
**What file is used by Docker Compose to define multi-container apps?**

A. Dockerfile
B. composefile.txt
C. docker-compose.yml
D. container.yml

**Answer:** C

---

## Question 8
**Which of the following is NOT a benefit of using Docker Compose?**

A. Managing multiple services easily
B. Starting all containers with a single command
C. Building Docker images manually
D. Defining networks and volumes declaratively

**Answer:** C

---

## Question 9
**Which layer of a Docker image is affected by the RUN instruction in a Dockerfile?**

A. Metadata only
B. Environment variables
C. A new intermediate image layer
D. Base kernel

**Answer:** C

---

## Question 10 
**What does the following command do?**

```bash
docker run -d -p 8080:80 nginx
```

A. Builds an image from the nginx Dockerfile
B. Runs an nginx container in detached mode and maps port 8080 on the host to 80 in the container
C. Updates the nginx container
D. Deletes the nginx image and contain

**Answer:** B
