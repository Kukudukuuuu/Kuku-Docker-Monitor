# Kuku Docker Monitor

A lightweight Dockerized monitoring dashboard built with Node.js.

## Features

* Live system monitoring dashboard
* Docker-ready setup
* Lightweight and simple
* Runs on LAN or localhost
* Beginner-friendly project structure

## Tech Stack

* Node.js
* HTML/CSS/JavaScript
* Docker

---

# Project Structure

```text
Kuku-Docker-Monitor/
├── Dockerfile
├── .dockerignore
├── package.json
├── package-lock.json
├── server.js
├── index.html
├── README.md
└── .gitignore
```

---

# Installation

## Clone Repository

```bash
git clone https://github.com/Kukudukuuuu/Kuku-Docker-Monitor.git
cd Kuku-Docker-Monitor
```

---

# Run Locally

Install dependencies:

```bash
npm install
```

Start server:

```bash
node server.js
```

Open browser:

```text
http://localhost:3001
```

---

# Docker Setup

## Build Docker Image

```bash
docker build -t kuku-docker-monitor .
```

## Run Docker Container

```bash
docker run -p 3001:3001 kuku-docker-monitor
```

Open:

```text
http://localhost:3001
```

---

# Dockerfile

```Dockerfile
FROM node:22-alpine

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

EXPOSE 3001

CMD ["node", "server.js"]
```

---

# .dockerignore

```text
node_modules
.git
npm-debug.log
```

---

# Git Workflow

Push updates:

```bash
git add .
git commit -m "update"
git push
```

Pull latest changes:

```bash
git pull
```

---

# Future Improvements

* Live graphs
* Docker container monitoring
* RAM/CPU charts
* WebSocket real-time updates
* Dark mode UI
* Reverse proxy support
* Multi-device monitoring
* Mobile responsive dashboard

---

# Docker Hub Usage

Pull image:

```bash
docker pull kukudukuuuu/kuku-docker-monitor
```

Run container:

```bash
docker run -p 3001:3001 kukudukuuuu/kuku-docker-monitor
```

Docker Compose example:

```yaml
services:
  monitor:
    image: kukudukuuuu/kuku-docker-monitor:latest

    ports:
      - "3001:3001"

    restart: unless-stopped
```

---

# Publishing To Docker Hub

Build image:

```bash
docker build -t kukudukuuuu/kuku-docker-monitor:latest .
```

Login:

```bash
docker login
```

Push image:

```bash
docker push kukudukuuuu/kuku-docker-monitor:latest
```

---

# License

MIT License


# License

MIT License

