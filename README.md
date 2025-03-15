### **Setup Instructions for `book4` (Vue + Tailwind CSS)**

---

## **📌 Project Setup (`book4`)**
This guide sets up a Vue 3 project with Vite and Tailwind CSS.

### **1️⃣ Install Node.js (if not installed)**
Ensure **Node.js (LTS version)** is installed. Check with:
```sh
node -v
npm -v
```
If missing, download from [Node.js Official Site](https://nodejs.org/).

---

### **2️⃣ Create Vue 3 Project with Vite**
Run the following command to create a Vue 3 project using Vite:
```sh
npm create vite@latest book4 --template vue
cd book4
npm install
```
---

### **3️⃣ Install Tailwind CSS**
Run:
```sh
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

---

### **4️⃣ Configure Tailwind CSS**
Edit **`tailwind.config.js`**:
```js
/** @type {import('tailwindcss').Config} */
export default {
  content: ["./index.html", "./src/**/*.{vue,js,ts,jsx,tsx}"],
  theme: {
    extend: {},
  },
  plugins: [],
};
```

Replace **`src/assets/main.css`** with:
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

---

### **5️⃣ Run the Development Server**
Start the project:
```sh
npm run dev
```
The site will be live at **`http://localhost:5173/`**.

---


