/mafici-web
 ├── public/
 │    ├── paginas-01.png
 │    ├── paginas-02.png
 │    ├── paginas-03.png
 │    ├── paginas-04.png
 │    ├── paginas-05.png
 │    ├── paginas-06.png
 │    ├── paginas-07.png
 │    ├── paginas-08.png
 │    └── paginas-09.png
 ├── src/
 │    ├── App.jsx
 │    ├── components/Navbar.jsx
 │    ├── index.css
 │    └── main.jsx
 ├── index.html
 ├── package.json
 ├── tailwind.config.js
 ├── postcss.config.js
 └── vite.config.js
{
  "name": "mafici-web",
  "version": "1.0.0",
  "private": true,
  "scripts": {
    "dev": "vite",
    "build": "vite build",
    "preview": "vite preview"
  },
  "dependencies": {
    "framer-motion": "^11.0.0",
    "react": "^18.0.0",
    "react-dom": "^18.0.0",
    "react-scroll": "^1.8.9"
  },
  "devDependencies": {
    "autoprefixer": "^10.4.0",
    "postcss": "^8.4.0",
    "tailwindcss": "^3.4.0",
    "vite": "^5.0.0"
  }
}
import { defineConfig } from 'vite'
import react from '@vitejs/plugin-react'

export default defineConfig({
  plugins: [react()],
  base: "./", // 👈 necesario para que funcione en Vercel
})
<!doctype html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <link rel="icon" type="image/svg+xml" href="/vite.svg" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>MAFICI - Festival Internacional de Cine</title>
  </head>
  <body>
    <div id="root"></div>
    <script type="module" src="/src/main.jsx"></script>
  </body>
</html>
import React from "react";
import ReactDOM from "react-dom/client";
import App from "./App";
import "./index.css";

ReactDOM.createRoot(document.getElementById("root")).render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);
