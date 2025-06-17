
# 🌍 WorldWise

**WorldWise** is a React application that helps you keep track of cities you've visited around the world. You can add, view, and delete cities with geographic details, all backed by a local fake REST API and styled using CSS Modules.

[![Live Demo](https://img.shields.io/badge/Live-Demo-blue?style=for-the-badge&logo=vercel)](https://world-wise-three-rho.vercel.app/app/cities)

---

## ✨ Features

- 🗺️ **Interactive Map** for exploring locations
- 🏙️ **City Management**:
  - View a list of saved cities
  - View detailed info for a specific city
  - Add and delete cities
- 🌍 **Geographic Details**: country name, flag emoji, notes, and coordinates
- 📦 **Context API & useReducer** for state management
- 🔄 **Fake REST API** with `json-server`
- 🎨 **Scoped Styling** using CSS Modules

---

## 🧱 Tech Stack

- React (Hooks, Context API)
- JavaScript (ES6+)
- CSS Modules
- `json-server`
- Vite
- Deployed on Vercel

---

## 📁 Project Structure

```

src/
├── components/
│   └── CityList.jsx
├── context/
│   ├── AuthContext.jsx
│   └── CitiesContext.jsx
├── pages/
│   └── MapPage.jsx
├── styles/
│   ├── App.module.css
│   └── City.module.css
├── App.jsx
└── main.jsx

````

---

## 🚀 Getting Started

### 1. Clone the Repo

```bash
git clone https://github.com/your-username/worldwise.git
cd worldwise
````

### 2. Install Dependencies

```bash
npm install
```

### 3. Start the Local API (json-server)

```bash
npm install -g json-server
json-server --watch data/db.json --port 9000
```

> The fake API runs at: `http://localhost:9000/cities`

### 4. Run the React App

```bash
npm run dev
```

---

## 📡 API Endpoints

* `GET /cities`
* `GET /cities/:id`
* `POST /cities`
* `DELETE /cities/:id`

### Sample Data (`db.json`)

```json
{
  "cities": [
    {
      "id": 13,
      "cityName": "Saint-Martin-la-Meanne",
      "country": "France",
      "emoji": "🇫🇷",
      "date": "2025-05-13T00:30:04.622Z",
      "notes": "wdwwawd",
      "position": {
        "lat": "45.14878312925081",
        "lng": "2.0044737210080004"
      }
    }
  ]
}
```

---

## 🧠 State Management (CitiesContext)

```js
const initialState = {
  cities: [],
  isLoading: false,
  currentCity: {},
  error: "",
};
```

Supported action types:

* `"loading"`
* `"cities/loaded"`
* `"city/loaded"`
* `"city/created"`
* `"city/deleted"`
* `"rejected"`

---

## 🌍 Live Demo

👉 [Click here to try it out!](https://world-wise-three-rho.vercel.app/app/cities)

---

## 🧪 Coming Soon

* User authentication flow
* Map markers for all cities
* Search & filter functionality
* Backend support for real data
* Responsive design improvements

---

## 🧾 License

MIT

---

## 👤 Author

**Anas Abdelhakim**
🔗 [LinkedIn](https://www.linkedin.com/in/anas-abdelhakim-548aa5268)
🐙 [GitHub](https://github.com/anasabdelhakim)


