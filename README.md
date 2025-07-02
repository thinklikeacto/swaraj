# Swaraj 🛕

**Swaraj** is a modular, production-grade microservices starter kit built for fast, clean, and scalable product development. It’s ideal for MVPs and real-world backend systems — blending structured monolith design with microservice-ready boundaries.

Unlike typical microservice starters, **Swaraj starts simple** — with a **single unified core service** for authentication, user management, and gateway logic — and scales gracefully as your product grows.

---

## 🌟 Key Highlights

- ✅ Combined `core-service` for auth, user, and API gateway
- ✅ Additional plug-and-play services: notifications, schedulers, ML, agentic AI
- ✅ Support for both Python (FastAPI) and Node.js (Express/Nest.js)
- ✅ Clean project layout with modular folders
- ✅ Independent DB containers per service (PostgreSQL, MongoDB, Redis)
- ✅ Kafka-ready for async event communication
- ✅ Docker-first setup (works out-of-the-box)

---

## 🛠 Tech Stack

| Layer         | Tools |
|---------------|-------|
| Backend       | Python (FastAPI), Node.js (Express/Nest) |
| Auth          | JWT (inside `core-service`) |
| Messaging     | Kafka / Redpanda |
| Databases     | PostgreSQL, MongoDB, Redis |
| Containerization | Docker, Docker Compose |
| Scheduling    | APScheduler / BullMQ / Node-Cron |
| ML & AI       | Python-based services (PyTorch, LangChain, Transformers, etc.) |
| Agentic AI    | LangGraph / LangChain + MCP (Model Context Protocol) |
| Migrations    | Alembic / Prisma |
| Testing       | Pytest / Jest |

---

## 🧱 Project Structure

### Microservices

```
swaraj/
├── core-service/                # Combines auth + user + API gateway logic
├── notification-service/       # For email/SMS/in-app events
├── process-engine/             # Cron-based or trigger-based scheduler
├── ml-service/                 # Model inference APIs (custom ML)
├── agentic-ai-service/         # LangChain/LangGraph-based agent system
├── shared-libs/                # Reusable logic (optional)
├── databases/
│   ├── postgres/
│   ├── mongodb/
│   └── redis/
└── docker-compose.yml
```

### Service Structure Template

```
microservice/
├── app/
│   ├── main.py / main.ts
│   ├── api/
│   ├── core/
│   ├── models/
│   ├── repository/
│   ├── services/
│   └── utils/
├── migrations/
├── tests/
├── Dockerfile
├── .env
└── README.md
```

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/your-org/swaraj.git
cd swaraj
```

### 2. Start All Services with Docker

```bash
docker-compose up --build
```

> Each service runs in its own container. Use ports or a unified gateway path for routing.

---

## 🛣 Roadmap

- [x] Unified core-service (auth + user + gateway)
- [x] Redis/Postgres/Mongo DB containers
- [x] Notification service scaffold
- [x] Process engine (scheduler) setup
- [ ] ML service starter (model loading, inference APIs)
- [ ] Agentic AI service with LangChain + MCP server
- [ ] Kafka integration across services
- [ ] Observability (Prometheus + Grafana)
- [ ] GitHub Actions CI/CD pipelines
- [ ] Helm charts for Kubernetes deployment

---

## 🔄 Design Philosophy

Swaraj balances simplicity and scale:

- Begin unified (fewer services, less complexity)
- Maintain clean boundaries per module
- Add or extract services as the product matures
- Use open standards (Docker, Kafka, REST, JWT, gRPC)
- Encourage developer clarity over early abstraction

---

## 🤝 Contributing

We welcome contributions of all kinds:

1. Fork the repo
2. Create a branch (`git checkout -b feature/my-feature`)
3. Make your changes
4. Open a PR

Please follow code standards and folder conventions per service type.

---

## 📄 License

Licensed under the [MIT License](./LICENSE)

---

## 🙏 Inspired By

- FastAPI, LangChain, NestJS, Kafka
- The spirit of **Swaraj** — self-governed, modular, and scalable systems
- Real-world needs of fast-moving product teams and startup builders

---

## 💬 Connect

For questions, ideas, or contributions — open an [Issue](https://github.com/thinklikeacto/swaraj/issues) or [Discussion](https://github.com/thinklikeacto/swaraj/discussions).

---
