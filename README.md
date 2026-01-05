# Hospital Management System

![Hospital Dashboard](images/home.png)

Hospital Management System is a modern, full-stack hospital management system designed with a premium aesthetic and high-performance architecture. It empowers healthcare providers with real-time tools for patient care, appointment scheduling, and administrative oversight.

## 🚀 Key Features

- **Real-time OPD Queue**: Instant synchronization between booking and doctor views using Socket.io.
- **Role-Based Command Center**: Specialized dashboards for Admins, Doctors, Lab Staff, and Patients.
- **Premium UX/UI**: Glassmorphism-inspired design with dynamic animations and fluid responsiveness.
- **One-Click Deployment**: Entire stack (Client + Server) runs in a single **Ubuntu 24.04** container.
- **HMS Naming Convention**: Unified `hms_app` and `hms_mongodb` for clear resource identification.
- **Secure Architecture**: JWT-based authentication with role-level authorization.

## 🛠️ Technology Stack

- **Frontend**: Next.js 16.1.1 (App Router), Tailwind CSS 4, Radix UI, TanStack Query.
- **Backend**: Node.js v22 (ESM), Express.js, TypeScript.
- **Database**: MongoDB v8.0.
- **Communication**: Socket.io for real-time WebSocket events.

---

## 🐳 Getting Started with Docker (Recommended)

The entire stack is managed via a single **unified HMS Dockerfile** at the root, which builds both client and server inside one container.

### Prerequisites

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

### Deployment Steps

1. **Clone the repository**:

   ```bash
   git clone https://github.com/rajanp1704/empyreal-hms.git
   cd empyreal-hms
   ```

2. **Configure Environment Variables**:
   Docker Compose uses pre-configured environment variables. You can modify them in `docker-compose.yml` if needed.

3. **Launch the stack**:

   ```bash
   docker compose up --build
   ```

4. **Access the application**:
   - **Frontend**: [http://localhost:3000](http://localhost:3000)
   - **Backend API**: [http://localhost:5000/api](http://localhost:5000/api)
   - **Swagger UI**: [http://localhost:5000/api-docs](http://localhost:5000/api-docs)

---

## 💻 Manual Setup

If you prefer to run the components separately for development:

### 1. Database

Ensure you have MongoDB v8 running locally on port `27017`.

### 2. Backend Server

```bash
cd server
npm install
# Create .env file based on .env.example
npm run dev
```

### 3. Frontend Client

```bash
cd client
npm install
# Create .env file based on .env.example
npm run dev
```

---

## 📄 Environment Variables Reference

### Backend (`/server/.env`)

| Variable      | Description         | Default                              |
| ------------- | ------------------- | ------------------------------------ |
| `PORT`        | Server port         | `5000`                               |
| `MONGODB_URI` | Connection string   | `mongodb://localhost:27017/hospital` |
| `JWT_SECRET`  | Secret key for auth | `your_secret`                        |
| `NODE_ENV`    | Environment mode    | `development`                        |

### Frontend (`/client/.env.local`)

| Variable              | Description         | Default                     |
| --------------------- | ------------------- | --------------------------- |
| `NEXT_PUBLIC_API_URL` | Public API endpoint | `http://localhost:5000/api` |

---

## 👨‍💻 Contributing

Contributions are welcome! Please read the `CONTRIBUTING.md` (if available) or simply open an Issue/PR.

## 📄 License

MIT License - see [LICENSE](LICENSE) for details.
