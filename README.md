# 🚀 NotificaJá API

**REST API service for the NotificaJá ecosystem**, built with Go and Gin framework.  
This service is responsible for receiving notification requests and publishing events to Apache Kafka.

---

## 📌 What is this?

This project serves as the **API layer** of the [NotificaJá](https://github.com/thalison/notificaja-streaming) system.  
It exposes HTTP endpoints to accept notification requests and then produces messages into Kafka topics.

Designed for scalability and easy integration with various clients.

---

## 🧪 Tech Stack

| Layer                 | Technology           |
|-----------------------|----------------------|
| Language              | Go (Golang)          |
| Web Framework         | Gin                  |
| Event Streaming       | Apache Kafka         |
| Configuration         | Environment variables (.env or YAML) |
| Authentication (future) | JWT                 |
| Containerization (future) | Docker + Compose  |

---

## 🧱 Project Structure

```
notificaja-api/
├── cmd/                    # Application entrypoint
│   └── main.go
├── internal/
│   ├── kafka/              # Kafka producer logic
│   ├── notification/       # Business logic and handlers
│   └── transport/          # HTTP handlers and routes (Gin)
├── configs/                # Configuration files
├── go.mod
└── README.md
```

---

## 🚀 How to Run (Development Mode)

1. Clone the repository:

```bash
git clone https://github.com/thalison/notificaja-api.git
cd notificaja-api
```

2. Install dependencies:

```bash
go mod tidy
```

3. Run the server:

```bash
go run cmd/main.go
```

4. Test the health endpoint:

```
GET http://localhost:8080/ping
```

---

## 📡 Kafka Topics (example)

| Topic Name       | Description                    |
|------------------|--------------------------------|
| `notifications`  | Topic where notification events are published |

---

## 🛠️ Features (WIP)

- [x] Project structure
- [x] Health check endpoint `/ping`
- [ ] Kafka producer implementation
- [ ] Notification request endpoint `/notify`
- [ ] JWT authentication
- [ ] Validation and error handling

---

## 🤝 Contributing

This project is open for learning and collaboration.  
Feel free to fork, open issues, or submit pull requests.

---

## 📄 License

MIT — free to use, modify, and learn from.

---

## 👨‍💻 Author

**Thalison Moreira da Silva**  
Building scalable notification systems, one event at a time.

