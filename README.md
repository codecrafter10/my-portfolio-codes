# Project Setup with Docker

This guide will help you set up and run the project using Docker.

---

## Prerequisites

- Install [Docker](https://docs.docker.com/get-docker/)
- (Optional but recommended) Install [Docker Compose](https://docs.docker.com/compose/install/)

Verify installation:

```bash
docker --version
docker compose version
Getting Started
1. Clone the Repository
bash
Copy code
git clone https://github.com/your-username/your-project.git
cd your-project
2. Build the Docker Image
bash
Copy code
docker build -t project-name .
3. Run the Container
bash
Copy code
docker run -d -p 3000:3000 project-name
-d runs the container in detached mode

-p 3000:3000 maps container port 3000 to local port 3000

Now, open http://localhost:3000 in your browser.

Using Docker Compose (Recommended)
If a docker-compose.yml file is provided:

1. Start Services
bash
Copy code
docker compose up --build -d
2. Stop Services
bash
Copy code
docker compose down
3. View Logs
bash
Copy code
docker compose logs -f
Common Commands
List running containers:

bash
Copy code
docker ps
Stop a container:

bash
Copy code
docker stop <container_id>
Remove a container:

bash
Copy code
docker rm <container_id>
Remove an image:

bash
Copy code
docker rmi project-name
Troubleshooting
If you face permission issues on Linux, add your user to the Docker group:

bash
Copy code
sudo usermod -aG docker $USER
Then log out and log back in.

To remove all containers and images (⚠️ use carefully):

bash
Copy code
docker system prune -a
