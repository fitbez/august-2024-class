# React + Vite

This project was bootstrapped with [Vite](https://vitejs.dev/) and React.

## 📌 Getting Started

### ✅ Prerequisites

Make sure you have [Node.js](https://nodejs.org/) installed (recommended version: `16.x` or later).

### 📦 Installation

1. **Create a new project using Vite**:

   ```sh
   npm create vite@latest my-app --template react

   cd my-app

   npm install

   npm run dev
   
##### Open your browser and go to: http://localhost:5173

📂 Project Structure
``````
my-app/
├── node_modules/        # Installed dependencies
├── public/              # Static assets (favicon, etc.)
│   ├── vite.svg
│   └── index.html       # Main HTML file
├── src/                 # Source files
│   ├── assets/          # Static assets (images, styles, etc.)
│   ├── App.css          # Global styles
│   ├── App.jsx (or App.tsx) # Main React component
│   ├── main.jsx (or main.tsx) # React entry file
│   ├── index.css        # Global styles
│   └── vite-env.d.ts    # TypeScript environment declaration (only in TS projects)
├── .gitignore           # Git ignore file
├── package.json         # Dependencies and scripts
├── vite.config.js (or vite.config.ts) # Vite configuration
├── README.md            # Project documentation
├── jsconfig.json (or tsconfig.json) # JavaScript/TypeScript config
``````
## 📝 Main Files and Their Purpose

### `index.html`
- Located in the `public/` directory.
- Acts as the entry point for the application.
- Contains a root `<div id="root"></div>` where the React app is mounted.

### `main.jsx` (or `main.tsx` for TypeScript)
- The entry file where React is initialized.
- Mounts the `<App />` component to the DOM.
``````
import React from 'react'
import ReactDOM from 'react-dom/client'
import App from './App'
import './index.css'

ReactDOM.createRoot(document.getElementById('root')).render(
  <React.StrictMode>
    <App />
  </React.StrictMode>,
)
``````

### `App.jsx` (or `App.tsx` for TypeScript)
- The main React component.
- Contains a simple starter UI.

```jsx
import { useState } from 'react'
import './App.css'

function App() {
  const [count, setCount] = useState(0)

  return (
    <div className="App">
      <h1>Hello Vite + React!</h1>
      <button onClick={() => setCount((count) => count + 1)}>
        Count is {count}
      </button>
    </div>
  )
}

export default App
