# 🍽 MealApp

> A recipe browser built with Flask and jQuery. Pick a category, browse the meals, open one for the full recipe and a cooking video.

One of my early Flask builds, kept around so the distance between then and now stays measurable.

---

## 🚀 Live Demo

**[mealapp-one.vercel.app](https://mealapp-one.vercel.app/)**

---

## ✨ Features

- **Category grid** — 14 meal categories pulled from TheMealDB
- **Filtered listing** — meals within a selected category
- **Recipe detail** — ingredients, instructions, area of origin, and an embedded YouTube cooking video
- **Server-rendered pages** — three routes, no client-side router

---

## 🧰 Tech Stack

| Layer | Technology |
|-------|-----------|
| Backend | Flask |
| Frontend | HTML / CSS |
| Interactivity | jQuery + AJAX |
| Data | [TheMealDB](https://www.themealdb.com/api.php) (public API) |
| Icons | Font Awesome 5 |
| Hosting | Vercel |

---

## 📁 Project Structure

```
mealapp/
├── app.py                    # Flask routes (3 endpoints)
├── public/
│   └── static/
│       └── style.css
├── templates/
│   ├── index.html            # category grid
│   ├── detail.html           # meals in a category
│   └── meal_detail.html      # full recipe + video
└── requirements.txt
```

The backend only renders templates. Every API call happens in the browser through jQuery, which is why there is no database and no server-side secrets.

---

## 🏁 Getting Started

```bash
# 1. Install dependencies
pip install -r requirements.txt

# 2. Run the development server
python app.py
```

Then open `http://localhost:5000`.

---

## ⚠️ Known Limitations

- Written in the jQuery era — no build step, no components, no state management
- No search, no pagination, no favourites
- TheMealDB is rate-limited and occasionally returns incomplete recipes
- Not optimised for very small screens

---

## 📜 History

Built as a project test using Flask, jQuery, AJAX, and Git/GitHub.

I keep it in my portfolio as a marker of where I started: a small server-rendered app that talks to a public API from the browser. My later projects moved to React with a proper build step, so the distance between this and today's work is easy to measure.
