# Docker Essentials Recap Quiz


### Question 1  
**What is one key difference between containers and virtual machines?**

A. Containers boot slower than VMs  
B. Containers run full operating systems  
C. Containers share the host OS kernel ✅  
D. Containers require hypervisors

---

### Question 2  
**What is the role of the Docker daemon in Docker's architecture?**

A. It runs inside containers to manage processes  
B. It manages images, containers, networks, and volumes ✅  
C. It builds Dockerfiles into HTML pages  
D. It provides a web UI for Docker containers

---

### Question 3  
**Which component does the `docker` CLI communicate with to execute commands?**

A. Docker Hub  
B. Linux Kernel  
C. Docker daemon ✅  
D. Container runtime

---

### Question 4  
**Which command prints a message and exits, proving Docker works?**

A. `docker run hello-world` ✅  
B. `docker build hello-world`  
C. `docker exec hello-world`  
D. `docker start hello-world`

---

### Question 5  
**In Docker, what is the purpose of `CMD` in a Dockerfile?**

A. Install dependencies  
B. Set environment variables  
C. Define the default command to run in the container ✅  
D. Copy files into the image

---

### Question 6  
**Which of the following is true about Docker images?**

A. Images are stored in containers  
B. Images are built in layers and cached ✅  
C. Images require a hypervisor  
D. Each image runs a full VM

---

### Question 7  
**What does the `depends_on` field do in `docker-compose.yml`?**

A. Assign IP addresses  
B. Control startup order of services ✅  
C. Connect containers to external volumes  
D. Mount local directories

---

### Question 8  
**What does `docker image prune` do?**

A. Removes unused images ✅  
B. Pauses running containers  
C. Lists current disk usage  
D. Kills the Docker daemon

---

### Question 9  
**What’s the correct order in the container lifecycle?**

A. run → stop → rm → start  
B. start → create → rm → stop  
C. create → start → stop → rm ✅  
D. rm → start → create → stop

---

### Question 10  
**What does a Docker health check in Compose do?**

A. Assigns a hostname  
B. Adds a new user  
C. Verifies the service is functioning properly ✅  
D. Forces the container to restart every minute
