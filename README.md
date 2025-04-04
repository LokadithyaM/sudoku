# 🧹 Sudoku Game (Next.js + MongoDB)

This project is a web-based **Sudoku puzzle game** built using **Next.js (App Router)** on the frontend and **MongoDB** for storing pre-generated puzzles and solutions.

---

## 🚀 Features

- Fetches a **random Sudoku puzzle** from MongoDB.
- Clean UI with **9x9 grid layout**.
- Puzzle and solution stored securely in database.
- Scalable architecture for adding features like solving, hints, difficulty levels.

---

## 📆 Tech Stack

- **Frontend**: Next.js 14+ (App Router, Client Components)
- **Backend**: Next.js API Routes (`app/api/grid/route.ts`)
- **Database**: MongoDB + Mongoose
- **Styling**: TailwindCSS

---

## 📁 Folder Structure

```
.
├── app/
│   └── api/
│       └── grid/
│           └── route.ts      # API route to fetch random puzzle
├── components/               # UI components (optional)
├── lib/
│   └── mongodb.ts            # MongoDB connection utility
├── models/
│   └── Sudoku.ts             # Mongoose schema/model
├── scripts/
│   └── insertPuzzles.ts      # Script to seed puzzles into DB
├── app/page.tsx              # Main game UI (client component)
└── README.md
```

---

## 💪 Setup & Installation

1. **Clone the repository**

```bash
git clone https://github.com/your-username/sudoku-nextjs.git
cd sudoku-nextjs
```

2. **Install dependencies**

```bash
npm install
```

3. **Add `.env.local`**

```env
MONGODB_URI=mongodb+srv://<username>:<password>@<cluster>.mongodb.net/sudokuDB
```

4. **Seed the database (optional)**

If you haven't added any puzzles yet, run:

```bash
ts-node scripts/insertPuzzles.ts
```

Or create a seed route to do this once via API.

5. **Run the development server**

```bash
npm run dev
```

Visit `http://localhost:3000` to view the app.

---

## 📄 Sample Data Format

In MongoDB, each document looks like:

```json
{
  "question": [[5, 3, 0, ...], [...], ...],
  "solution": [[5, 3, 4, ...], [...], ...]
}
```

---

## 🧐 Future Enhancements

- Input cells to play Sudoku interactively.
- Sudoku solver and hint system.
- Difficulty levels (easy, medium, hard).
- Timer and scoring.
- Leaderboard and user accounts.

---

## 🤝 Contributing

1. Fork this repo.
2. Create a new branch.
3. Commit and push your changes.
4. Open a pull request.

---
