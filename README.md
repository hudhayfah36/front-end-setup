# Setting Up Next.js and React.js Projects Using Vite

## 1. Install Node.js

Before starting, ensure you have **Node.js** installed.

- **Windows**: Download and install from [Node.js official website](https://nodejs.org/).
- **Linux**:
  ```sh
  sudo apt update && sudo apt install nodejs npm -y
  ```
  To check the installed version:
  ```sh
  node -v
  ```

---

## 2. Initialize a Vite Project

### For React.js

Run the following commands:

```sh
# Create a React project
npm create vite@latest my-react-app --template react

# Move into the project folder
cd my-react-app

# Install dependencies
npm install
```

### For Next.js

Run:

```sh
# Create a Next.js project
npm create vite@latest my-next-app --template nextjs

# Move into the project folder
cd my-next-app

# Install dependencies
npm install
```

---

## 3. Install Tailwind CSS

Inside the project directory, run:

```sh
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

### Configure Tailwind in `tailwind.config.js`

Open `tailwind.config.js` and update the `content` section:

```js
/** @type {import('tailwindcss').Config} */
export default {
  content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
};
```

### Add Tailwind to CSS

In `src/index.css` (React) or `src/globals.css` (Next.js), add:

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

---

## 4. Run the Project

To start the development server, use:

```sh
npm run dev
```

- Open [http://localhost:5173](http://localhost:5173) for React.
- Open [http://localhost:3000](http://localhost:3000) for Next.js.

---

## 5. Project Structure and File Placement

### React.js
- **Components** go inside `src/components/`.
- **Pages** are usually inside `src/pages/`.
- Example structure:
  ```
  src/
  ├── components/
  │   ├── Header.jsx
  │   ├── Footer.jsx
  ├── pages/
  │   ├── Home.jsx
  │   ├── About.jsx
  │
  ├── App.jsx  # Main component
  ├── main.jsx  # Entry point
  ```

### Next.js
- **Pages** go inside the `pages/` directory (automatically routes URLs).
- **Components** should be inside `components/`.
- Example structure:
  ```
  src/
  ├── components/
  │   ├── Navbar.jsx
  │   ├── Footer.jsx
  ├── pages/
  │   ├── index.jsx  # Home page
  │   ├── about.jsx  # About page
  ```

---

## 🎉 You're Ready to Start Building!
