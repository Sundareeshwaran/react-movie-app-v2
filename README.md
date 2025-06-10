
# 🇮🇳 React Movie App - Indian Movie Explorer 🎬

A React-based movie discovery app that helps users find trending and popular Indian movies. It integrates with [The Movie Database (TMDB)](https://www.themoviedb.org/) API and supports search, trending section, and seamless IMDb redirection.

## ✨ Features

- 🔍 Search movies by name (filtered to Indian languages)
- 📈 View trending Indian movies
- 🎞️ Discover popular Indian movies
- ⚡ Debounced search to reduce API calls
- ⏳ Loading spinner during API calls
- 📊 Search analytics (using Appwrite)
- 📦 Built with modern React best practices

---

## 🔧 Tech Stack

- **Frontend:** React, Tailwind CSS
- **Data Source:** TMDB API
- **Backend Services:** Appwrite (for tracking search analytics)
- **Utility Libraries:** `react-use` for debounce

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Sundareeshwaran/react-movie-app-v2
cd react-movie-app
```

### 2. Install dependencies

```bash
npm install
```

### 3. Set up Environment Variables

Create a `.env` file in the root directory and add your TMDB Bearer token:

```
VITE_TMDB_API_KEY=your_tmdb_read_access_token
```

> ⚠️ Use the **Bearer token** (Read Access Token) from TMDB, not the plain API key.

---

## 📁 Project Structure

```
src/
├── components/
│   ├── Search.jsx
│   ├── Spinner.jsx
│   └── MovieCard.jsx
├── App.jsx
├── main.jsx
├── appwrite.js
└── ...
```

---

## 🌍 API Usage

### ✅ Discover Indian Movies

```
GET /discover/movie?sort_by=popularity.desc&region=IN&language=en-US&with_origin_country=IN
```

### 🔍 Search Indian Movies

```
GET /search/movie?query=QUERY&region=IN&language=en-US
```

Then filtered manually using:

```js
original_language in ["hi", "ta", "te", "ml", "kn", "mr", "bn", "pa"]
```

---

## 📊 Appwrite Integration

The app uses Appwrite to log search analytics.

- Set up Appwrite backend
- Use `updateSearchCount(query, movie)` to store data
- Customize `appwrite.js` as per your backend config

---

## 🧠 Improvements (Future Scope)

- 🎯 Genre filtering (e.g., Action, Comedy)
- 🎬 Trailer preview
- 🌐 Multi-language support
- 🗂 Pagination
- 🔥 Auto-complete suggestions

---

## 📜 License

MIT License. Feel free to fork and customize!

---

## 🙌 Acknowledgements

- [The Movie Database (TMDB)](https://www.themoviedb.org/)
- [Appwrite](https://appwrite.io/)
- [React](https://reactjs.org/)

---

## 👨‍💻 Author

Made with ❤️ by Sundareeshwaran
