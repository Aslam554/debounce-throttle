# ⚡ Debounce & Throttle Demo

![HTML](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

> An interactive vanilla JavaScript demo that visually compares **Normal**, **Debounce**, and **Throttle** input handling — a must-know for every JavaScript developer.

---

## 🚀 Getting Started

### Prerequisites
- [Node.js](https://nodejs.org/) (v14 or higher)

### Installation & Run

```bash
# 1. Clone the repository
git clone https://github.com/Aslam554/debounce-throttle.git

# 2. Move into the project
cd debounce-throttle

# 3. Install dependencies
npm install

# 4. Start the dev server
npm start
```

> Opens automatically at **http://localhost:3000** 🎉

---

## 🎮 How It Works

Type in the search box and switch between the three modes to see how each one behaves:

| Mode | Behaviour | Best Used For |
|------|-----------|--------------|
| **Normal** | Fires on **every** keystroke | — |
| **Debounce** | Waits **500ms** after you stop typing | Search inputs, form validation |
| **Throttle** | Fires at most **once every 500ms** | Scroll events, mouse move |

---

## 🛠️ Scripts

| Command | Description |
|---------|-------------|
| `npm start` | Start local server on port 3000 and open browser |
| `npm run dev` | Same as `npm start` |

---

## 🧠 Core Concepts

### 🔵 Debounce
Delays execution until **after** the user stops performing an action for a set time.

```js
function debounce(fn, delay) {
  let timer;
  return function (...args) {
    clearTimeout(timer);
    timer = setTimeout(() => fn.apply(this, args), delay);
  };
}
```

### 🟠 Throttle
Ensures a function is called **at most once** within a given time window.

```js
function throttle(fn, limit) {
  let lastCall = 0;
  return function (...args) {
    const now = Date.now();
    if (now - lastCall >= limit) {
      lastCall = now;
      fn.apply(this, args);
    }
  };
}
```

---

## 📁 Project Structure

```
debounce-throttle/
├── index.html          # Main demo page (HTML + CSS + JS)
├── package.json        # npm config & scripts
├── package-lock.json   # Dependency lock file
├── .gitignore          # Ignores node_modules & OS files
└── README.md           # You're here!
```

---

## 👤 Author

**Aslam554** — [GitHub](https://github.com/Aslam554)

---

## 📄 License

MIT © [Aslam554](https://github.com/Aslam554)
