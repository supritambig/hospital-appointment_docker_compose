# 🏥 Hospital Appointment System (Dockerized)

A **Spring Boot + MySQL** based Hospital Appointment application fully containerized using Docker and Docker Compose.

---

# 🚀 Tech Stack

* Java, Spring Boot
* MySQL
* Maven
* Docker
* Docker Compose

---

# 🐳 Run Application

## Clone Repo

```bash
git clone <your-repo-url>
cd hospital-appointment
```

---

## Download Wait Script

```bash
curl -o wait-for-it.sh https://raw.githubusercontent.com/vishnubob/wait-for-it/master/wait-for-it.sh
chmod +x wait-for-it.sh
```

---

## Run Containers

```bash
docker compose up --build
```

---

## Access App

```bash
http://localhost:8085
```

---

# 📦 Useful Commands

## Start

```bash
docker compose up --build
```

## Background Run

```bash
docker compose up -d --build
```

## Stop

```bash
docker compose down
```

## Reset DB

```bash
docker compose down -v
```

## Logs

```bash
docker compose logs -f
```

---

# 🧹 Cleanup (Fix Errors)

```bash
docker rm -f java-app mysql-db
docker volume rm hospital-appointment_docker_compose_db-data
docker system prune -a
```

---

# ⚠️ Common Issues

## DB Connection Error

* Use `db` (not localhost)

## Port Issue

```bash
server.port=8085
```

## Check Logs

```bash
docker logs java-app
```

---

# 👨‍💻 Author

Suprit Ambig
