# MyShelf

<img width="1440" height="777" alt="login-page" src="https://github.com/user-attachments/assets/12f896a4-7db5-44fa-b2a9-14b0c0bc8725" />
<img width="1440" height="779" alt="discover-next-book" src="https://github.com/user-attachments/assets/824ee359-3e80-4d64-8d49-a828384fc38f" />
<img width="1440" height="773" alt="book-catalog" src="https://github.com/user-attachments/assets/d2f87d45-f2f9-4a37-8d1e-6120275fdc8f" />
<img width="1440" height="770" alt="my-bookshelf" src="https://github.com/user-attachments/assets/45f741d7-dfe9-4023-8ea2-d15e8f9ec332" />
<img width="1440" height="774" alt="profile" src="https://github.com/user-attachments/assets/8d0731ab-b380-44ac-9112-7b95bec06ee1" />
<img width="1440" height="774" alt="book-clubs" src="https://github.com/user-attachments/assets/0b9f9d2b-2c80-4a7c-ab87-7ba7323614ed" />
<img width="1440" height="772" alt="group-discussion" src="https://github.com/user-attachments/assets/f9e4c446-30da-49c0-8b76-9281dec3fd55" />
<img width="1399" height="676" alt="new-discussion" src="https://github.com/user-attachments/assets/99f843d7-ca33-44c3-98b4-26a3e4a35052" />



A scalable Goodreads-like web application for book discovery, rating, reviewing, tracking reading status, social connections, book clubs, and personalized recommendations.
Deployed on Render. Link: https://goodreads-frontend-rp56.onrender.com/login
## Features
- User registration and login (JWT authentication)
- Book catalog with search and pagination
- Add books to personal bookshelf with status: Want to Read, Currently Reading, Read
- View and manage your bookshelf
- Update reading status or remove books from shelf
- **Community features:**
  - Create and join book clubs/groups
  - Start discussions and reply to topics
  - Search and browse groups by name, description, or tags
  - View group members and discussions
- Social features (book clubs, friends) 

## Tech Stack
- **Backend:** Node.js, Express, MongoDB, Mongoose, JWT
- **Frontend:** React, Next.js (App Router), TypeScript
---

## Backend Setup

1. **Install dependencies:**
   ```sh
   cd backend
   npm install
   ```
2. **Configure environment:**
   - Copy `.env.example` to `.env`.
3. **Start the server:**
   ```sh
   npm run dev
   ```
   The backend runs on [http://localhost:5000](http://localhost:5000)
   
## Frontend Setup

1. **Install dependencies:**
   ```sh
   cd frontend
   npm install
   ```
2. **Start the frontend:**
   ```sh
   npm run dev
   ```
   The frontend runs on [http://localhost:3000](http://localhost:3000)

---

## Usage
- Register or log in
- Browse the book catalog
- Add books to your shelf and update their status
- View and manage your bookshelf
- Create or browse topics in community and add posts
- View others' profiles and follow others

---

## Development
- Backend: `cd backend && npm run dev`
- Frontend: `cd frontend && npm run dev`


