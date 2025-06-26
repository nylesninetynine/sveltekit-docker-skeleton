# 🧪 SvelteKit + Prisma + MariaDB Docker Skeleton

This is a boilerplate project to quickly spin up a full-stack SvelteKit app backed by MariaDB and Prisma, all running in Docker.

---

## 🚀 Quick Start

### 1. Clone the Repo

```bash
git clone https://github.com/YOUR_USERNAME/sveltekit-docker-skeleton.git
cd sveltekit-docker-skeleton
```
## 2. Create env file (optional: adjust db variables)
```bash
cp .example.env .env
```
## 3. Start docker containers
```bash
docker-compose up --build
```
### 4. Run initial Prisma migration
```bash
docker exec -it <your_app_container_name> npx prisma migrate dev --name init
```
Or if using the default container name:
```bash
docker exec -it sveltekit-1 npx prisma migrate dev --name init
```

### 📦 What’s Included
	•	SvelteKit
	•	Prisma ORM
	•	MariaDB (via Docker)
	•	Dockerized development workflow

### Project structure:
.
├── src/                # SvelteKit source
├── prisma/             # Prisma schema & migrations
├── Dockerfile          # App container
├── docker-compose.yml  # Docker services (SvelteKit + MariaDB)
├── .env.example        # Sample env config
├── .gitignore
└── README.md
