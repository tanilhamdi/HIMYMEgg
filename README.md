# 🥚 HIMYM Egg

> *“Because sometimes you just need a random episode of How I Met Your Mother, and sometimes... well, you get something else.”*

A lightweight Svelte single-page application that picks a random *How I Met Your Mother* episode link from a local text file and redirects you instantly. Built with Svelte, TypeScript, and a subtle dose of chaos.

---

## 🚀 Features

- **Random Episode Picker:** Grabs a random line from `himym.txt` using Lodash.
- **Easter Egg:** Includes a special chance trigger for when luck isn't quite on your side.
- **Svelte + Vite:** Lightning-fast setup and rendering.
- **Dark Mode UI:** Sleek, modern dark-themed interface styled with custom CSS and a vibrant accent.

---

## 🛠️ Tech Stack

- **Framework:** [Svelte](https://svelte.dev/) (with TypeScript)
- **Utility:** [Lodash](https://lodash.com/) (`_.random`)
- **Styling:** Vanilla CSS (Flexbox, custom gradients, responsive layout)

---

## 📦 Getting Started

Follow these instructions to get a local copy up and running on your machine.

### Prerequisites

Make sure you have **Node.js** and **npm** (or yarn/pnpm/bun) installed.

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/tanilhamdi/HIMYMEgg.git
   cd HIMYMEgg
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Run the development server:**
   ```bash
   npm run dev
   ```

4. Open your browser and navigate to the local development URL provided by Vite.

---

## 📝 Configuration

- The app reads episode URLs/paths from a raw text file located at `./himym.txt` (`?raw` import via Vite). Ensure your list contains valid links line by line.

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.