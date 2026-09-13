# MyShelf

Full-stack social reading app: catalog + Google Books import, personal shelves, follows, and book-club discussions.

**[Live demo](https://goodreads-frontend-rp56.onrender.com/login)** · Render free tier — first load can take ~30s

| Layer | Choices |
| --- | --- |
| Frontend | Next.js 15 (App Router), React 19, TypeScript, Zustand, Axios |
| Backend | Node.js (ESM), Express, Mongoose, JWT in httpOnly cookies |
| Data | MongoDB — compound unique indexes, text indexes, aggregation |
| Tests | Jest, Supertest, `mongodb-memory-server` |
| Deploy | Split frontend/backend on Render, credentialed CORS |

---


---

## Product

| Area | What you can do |
| --- | --- |
| Catalog | Browse paginated books; search Google Books and import a result onto the shelf |
| Shelf | Want to read / currently reading / read; rating + review; remove |
| Social | Public profiles, follow/unfollow, view another reader's shelf by status |
| Clubs | Create/join groups, start topics, reply in-thread |

```
Next.js (Render)  --cookie JWT-->  Express API (Render)
                                      |            \
                                      v             v
                                   MongoDB     Google Books API
```

---

## Screenshots

<p>
  <img width="48%" alt="Login" src="https://github.com/user-attachments/assets/12f896a4-7db5-44fa-b2a9-14b0c0bc8725" />
  <img width="48%" alt="Discover" src="https://github.com/user-attachments/assets/824ee359-3e80-4d64-8d49-a828384fc38f" />
</p>
<p>
  <img width="48%" alt="Catalog" src="https://github.com/user-attachments/assets/d2f87d45-f2f9-4a37-8d1e-6120275fdc8f" />
  <img width="48%" alt="Bookshelf" src="https://github.com/user-attachments/assets/45f741d7-dfe9-4023-8ea2-d15e8f9ec332" />
</p>
<p>
  <img width="48%" alt="Profile" src="https://github.com/user-attachments/assets/8d0731ab-b380-44ac-9112-7b95bec06ee1" />
  <img width="48%" alt="Book clubs" src="https://github.com/user-attachments/assets/0b9f9d2b-2c80-4a7c-ab87-7ba7323614ed" />
</p>
<p>
  <img width="48%" alt="Discussion" src="https://github.com/user-attachments/assets/f9e4c446-30da-49c0-8b76-9281dec3fd55" />
  <img width="48%" alt="New discussion" src="https://github.com/user-attachments/assets/99f843d7-ca33-44c3-98b4-26a3e4a35052" />
</p>

---

## API (authenticated routes marked)

| | Method | Path |
| --- | --- | --- |
| Auth | `POST` | `/api/users/register` · `/login` · `/logout` |
| | `GET` `PUT` | `/api/users/profile` |
| Shelf | `GET` `POST` | `/api/users/bookshelf` |
| | `PUT` `DELETE` | `/api/users/bookshelf/:id` |
| | `GET` | `/api/users/:id/bookshelf` · `/bookshelf/stats` |
| Social | `GET` | `/api/users/:id` · `/followers` · `/following` |
| | `GET` `POST` `DELETE` | `/api/users/:id/follow` · `/follow-status` |
| Books | `GET` `POST` | `/api/books` · `/api/books/import` · `/api/books/search/external` |
| Clubs | `GET` `POST` | `/api/groups` · `/api/groups/:id/join` · `/leave` |
| Topics | `GET` `POST` | `/api/groups/:id/topics` · `/api/topics/:id` · `/reply` |

---

## Run locally

```sh
# API — http://localhost:5000
cd backend
cp .env.example .env   # MONGODB_URI, JWT_SECRET
npm install
npm run dev

# Web — http://localhost:3000
cd frontend
npm install
npm run dev            # NEXT_PUBLIC_API_URL defaults to http://localhost:5000/api
```

```sh
cd backend && npm test
```

`.env.example` keys: `PORT`, `MONGODB_URI`, `JWT_SECRET`, `NODE_ENV`, `CLIENT_URL`.
