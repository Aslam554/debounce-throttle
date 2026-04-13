# ⚡ Debounce & Throttle Demo

An interactive vanilla JavaScript demo that visually compares **Normal**, **Debounce**, and **Throttle** input handling — perfect for understanding these core performance optimization concepts.

---

## 🚀 Getting Started

### Prerequisites
- [Node.js](https://nodejs.org/) (v14 or higher)
- npm (comes with Node.js)

### Installation & Run

```bash
# 1. Clone the repository
git clone https://github.com/Aslam554/debounce-throttle.git
cd debounce-throttle

# 2. Install dependencies
npm install

# 3. Start the dev server
npm start
```

The app will automatically open at **http://localhost:3000** in your browser.

---

## 📖 What's Inside

| Mode | Behaviour |
|------|-----------|
| **Normal** | Fires an API call on **every** keystroke |
| **Debounce** | Waits **500ms** after you stop typing, then fires once |
| **Throttle** | Fires at most **once every 500ms** while you type |

---

## 🛠️ Scripts

| Command | Description |
|---------|-------------|
| `npm start` | Start local server on port 3000 and open browser |
| `npm run dev` | Same as `npm start` |

---

## 🧠 Concepts

### Debounce
> Delays execution until after a user has stopped performing an action for a specified time. Great for **search inputs**, **form validation**, and **resize events**.

```js
function debounce(fn, delay) {
  let timer;
  return function (...args) {
    clearTimeout(timer);
    timer = setTimeout(() => fn.apply(this, args), delay);
  };
}
```

### Throttle
> Ensures a function is called at most once in a specified time window. Great for **scroll events**, **mouse move**, and **window resize**.

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
├── index.html       # Main demo page
├── package.json     # npm config & scripts
└── README.md        # You're here!
```

---

## 📄 License

MIT © [Aslam554](https://github.com/Aslam554)
