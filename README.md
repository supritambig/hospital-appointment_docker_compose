# 🏥 Hospital Appointment System (Dockerized)

A **Spring Boot + MySQL** based Hospital Appointment application fully containerized using Docker and Docker Compose with proper service orchestration.

---

# 🚀 Tech Stack

* **Backend:** Java, Spring Boot
* **Database:** MySQL
* **Build Tool:** Maven
* **Containerization:** Docker
* **Orchestration:** Docker Compose

---

# 📁 Project Structure

```
.
├── Dockerfile
├── docker-compose.yml
├── wait-for-it.sh
├── pom.xml
├── src/
└── README.md
```

---

# ⚙️ Prerequisites

Make sure you have installed:

* Docker
* Docker Compose

Verify installation:

```
docker --version
docker compose version
```

---

# 🐳 How to Run the Application

## 1️⃣ Clone the Repository

```
git clone <your-repo-url>
cd hospital-appointment
```

---

## 2️⃣ Download Wait Script (IMPORTANT)

```
curl -o wait-for-it.sh https://raw.githubusercontent.com/vishnubob/wait-for-it/master/wait-for-it.sh
```

---

## 3️⃣ Build and Run Containers

```
docker compose up --build
```

---

## 4️⃣ Access the Application

Open in browser:

```
http://localhost:8085
```

---

# 🗄️ Database Configuration

| Property | Value |
| -------- | ----- |
| Host     | db    |
| Port     | 3306  |
| Database | mydb  |
| Username | root  |
| Password | root  |

---

# 🔄 Application Flow

1. MySQL container starts
2. Database initializes
3. `wait-for-it.sh` waits for DB readiness
4. Spring Boot app starts
5. App connects to MySQL
6. Application becomes available

---

# 📦 Useful Commands

## Start application

```
docker compose up --build
```

## Run in background

```
docker compose up -d --build
```

## Stop application

```
docker compose down
```

## Remove volumes (reset DB)

```
docker compose down -v
```

## View logs

```
docker compose logs -f
```

---

# ⚠️ Common Issues & Fixes

## ❌ Database connection error

* Ensure MySQL is running
* Check DB URL uses `db` (not localhost)

---

## ❌ Port not accessible

* Ensure:

```
server.port=8085
```

---

## ❌ Container crashes

Check logs:

```
docker logs java-app
```

---

# 🧠 Key Concepts

* Service name (`db`) acts as hostname
* Multi-stage Docker build reduces image size
* `wait-for-it.sh` ensures DB readiness
* Docker Compose manages networking automatically

---

# 🚀 Future Enhancements

* Add Redis caching
* Add Nginx reverse proxy
* CI/CD using Jenkins
* Kubernetes deployment

---

# 👨‍💻 Author

Suprit Ambig
