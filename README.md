# Setting Up a React.js Project Using Vite (Windows) for Students

## 1. Install Node.js

Before starting, you need to install **Node.js**.

- **Download and install** from [Node.js official website](https://nodejs.org/).
- To check if Node.js is installed, open **Command Prompt (cmd)** and run:
  ```sh
  node -v
  ```

---

## 2. Create a React.js Project Using Vite

1. Open **Command Prompt (cmd)** and run:
   ```sh
   npm create vite@latest my-react-app --template react
   ```
   Replace `my-react-app` with your project name.

2. Move into the project folder:
   ```sh
   cd my-react-app
   ```

3. Install dependencies:
   ```sh
   npm install
   ```

---

## 3. Install Tailwind CSS

Inside the project folder (`my-react-app`), run:

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

Open `src/index.css` and add:

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

---

## 4. Run the Project

To start the development server, run:

```sh
npm run dev
```

- Open [http://localhost:5173](http://localhost:5173) in your browser.

---

## 5. Project Structure (Where to Place Components)

- **Components** go inside the `src/components/` folder.
- Example structure:
  ```
  src/
  ├── components/
  │   ├── Header.jsx
  │   ├── Footer.jsx
  ├── App.jsx  # Main component
  ├── main.jsx  # Entry point
  ```

---

## 🎉 You Are Ready to Start Coding!
