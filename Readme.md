<!-- prettier-ignore -->
<p align="center">
  <img alt="Expense Tracker" src="https://img.shields.io/badge/Expense%20Tracker-🚀-7F00FF?style=for-the-badge&logo=appveyor" />
  <br />
  <img alt="stack" src="https://img.shields.io/badge/React-17.x-61DAFB?logo=react&logoColor=white&style=flat-square" />
  <img alt="stack" src="https://img.shields.io/badge/Node.js-18.x-539E43?logo=node.js&logoColor=white&style=flat-square" />
  <img alt="stack" src="https://img.shields.io/badge/MongoDB-6.x-4EA94B?logo=mongodb&logoColor=white&style=flat-square" />
  <img alt="stack" src="https://img.shields.io/badge/Vite-4.x-646CFF?logo=vite&logoColor=white&style=flat-square" />
  <img alt="license" src="https://img.shields.io/badge/License-MIT-brightgreen?style=flat-square" />
</p>

## Expense Tracker

A simple full-stack Expense Tracker app (React + Node/Express + MongoDB) with user authentication, income & expense management, charts, file uploads and basic dashboard analytics.


<div align="center">

### 🤝 Get in Touch

For inquiries or collaboration opportunities, reach out via:

</div>

<div align="center">

| 📧 **Email** | [sidhusidharth7075@gmail.com](mailto:sidhusidharth7075@gmail.com) |
| 💼 **LinkedIn** | [LohithSappa](https://www.linkedin.com/in/lohith-sappa-aab07629a/) |

</div>

---

<div align="center">

⭐ **Don't forget to star this repository if you found it helpful!** ⭐

**Made with ❤️**

[![GitHub stars](https://img.shields.io/github/stars/sidhusidharth7075/expense-tracker?style=social&label=Star)](https://github.com/sidhusidharth7075/expense-tracker)
[![GitHub forks](https://img.shields.io/github/forks/sidhusidharth7075/expense-tracker?style=social&label=Fork)](https://github.com/sidhusidharth7075/expense-tracker)

</div>

give star to repo if it is useful
## Highlights ✨

- Authentication (JWT)
- CRUD for incomes and expenses
- File uploads (profile images) served from `/uploads`
- Small dashboard endpoints that aggregate recent transactions and chart data
- Frontend: React + Vite + Tailwind + Recharts
- Backend: Node.js + Express + MongoDB (Mongoose)

## Repo structure 📁

- `backend/` — Express API, MongoDB models, controllers, and uploads
  - `server.js` — app entrypoint
  - `config/db.js` — Mongo connection
  - `controllers/` — auth, income, expense, dashboard logic
  - `models/` — `User`, `Income`, `Expense`
  - `routes/` — route definitions mounted under `/api/v1/*`
  - `uploads/` — static files (profile images, etc.)
  - `expense_details.xlsx`, `income_details.xlsx` — sample spreadsheets

- `frontend/expense-tracker/` — React app (Vite)
  - `src/` — components, pages, hooks and utilities

## Tech stack 🛠️

- Backend: Node.js, Express, Mongoose, JWT, multer, bcryptjs, xlsx
- Frontend: React, Vite, React Router, Tailwind CSS, Recharts, axios

## Quick start (Windows / PowerShell)

1) Clone the repo and open a terminal in the workspace root.

2) Backend

  - Install deps and start dev server (colors preserved for readability):

```powershell
cd backend; npm install; npm run dev
```

  - Production start (after setting env):

```powershell
cd backend; npm install --production; npm start
```

3) Frontend

  - Install deps and run the dev server:

```powershell
cd frontend\expense-tracker; npm install; npm run dev
```

  - Build for production:

```powershell
cd frontend\expense-tracker; npm run build
```

## Environment variables (backend) 🔑

Create a `.env` file in `backend/` with the following (example):

```
MONGO_URI=mongodb://localhost:27017/expense-tracker
JWT_SECRET=your_jwt_secret
CLIENT_URL=http://localhost:5173
PORT=5000
```

Notes:
- `CLIENT_URL` is used by CORS middleware. Set it to your frontend dev URL (Vite default is `http://localhost:5173`).
- JWT tokens issued by the backend expire in 1 hour by default.

## API overview 🔍

Base URL: `http://localhost:5000/api/v1`

- Auth
  - `POST /auth/register` — register user (returns token)
  - `POST /auth/login` — login (returns token)
  - `GET /auth/me` — get user info (protected)

- Income
  - Standard CRUD routes under `/income` (protected)

- Expense
  - Standard CRUD routes under `/expense` (protected)

- Dashboard
  - Aggregation endpoints under `/dashboard` for charts and recent transactions (protected)

Uploads are served statically at `/uploads` (e.g., `http://localhost:5000/uploads/<filename>`).

Refer to the backend `routes/` and `controllers/` for full endpoint details and request/response shapes.

## Useful developer notes

- Database: the project uses Mongoose models located in `backend/models`.
- Passwords are hashed (bcryptjs) on the User model; login uses a compare helper.
- Multer handles image uploads; uploaded files land in `backend/uploads` and are exposed via express.static.
- There are sample Excel files in `backend/` (`expense_details.xlsx` and `income_details.xlsx`) — the backend includes `xlsx` dependency if you want to import/export.

## Running locally — checklist

1. MongoDB running locally or a remote URI set in `MONGO_URI`.
2. `.env` created in `backend/` with required vars.
3. Start backend, then frontend.

## Tests

There are no automated tests included. Adding unit/integration tests (Jest + Supertest for backend, React Testing Library for frontend) is a recommended next step.

## Contributing

Contributions are welcome. Open an issue to discuss features or bug fixes. Keep PRs small and focused.

## License

MIT

---

If you'd like, I can also:
- add a short API reference (example requests + sample responses),
- add a Postman/Insomnia collection,
- or create a minimal `docker-compose` for Mongo + backend + frontend.

---

give star to repo if it is useful
