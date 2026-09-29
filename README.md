# TaskScheduler 🚀
A high-performance, containerized task scheduling and execution engine built using a polyglot microservice architecture. 

### Architecture & Tech Stack
* **API Gateway:** Node.js / Express (Handles job intake and enqueueing)
* **Message Broker & Queue:** Redis (`BRPOP` atomic queue)
* **Worker Engine:** Multi-threaded Java 17 worker pool (concurrently processes jobs using true multithreading)
* **Persistence:** PostgreSQL (Tracks job state and execution status)
* **Infrastructure:** Docker & Docker Compose (Multi-stage builds, isolated container networks)

### Key Features
* Asynchronous event-driven job processing decoupling ingestion from execution.
* True concurrency via a Java ExecutorService thread pool processing tasks safely from a shared Redis queue.
* Fully containerized and orchestratable with a single `docker-compose up` command.
