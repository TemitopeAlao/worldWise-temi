# WordWise

WordWise is a React-based project built as part of my learning journey.
It helped me practice **React Router, Context API, authentication, protected routes, state management**, and **performance optimization** in a real-world style application.

---

## 🚀 What I Learned

Working on WordWise gave me hands-on experience with:

- Setting up routes with **React Router v6**.
- Creating and using **Context API** for global state.
- Handling **fake authentication** (login, logout, protected routes).
- Using **useEffect + navigate** for redirects after login.
- Protecting routes with a custom `ProtectedRoute` component.
- Implementing **route-based code splitting** with `React.lazy` and `Suspense` to reduce initial bundle size.
- Building a layout with shared components (e.g., Sidebar, Map, User).
- Writing cleaner, modular React code.

This project also deepened my understanding of how authentication flows and performance optimization work in React.

---

## 📂 Features

- **Login / Logout system** with fake user credentials.
- **Protected dashboard** (`/app`) only accessible after login.
- **User info display** (name + avatar).
- **Route protection** using a custom component.
- **Navigation** with React Router.
- **Optimized bundle size** via code splitting for faster load times.

---

## 🛠️ Tech Stack

- **React** (with hooks)
- **React Router v6**
- **Context API** for state management
- **CSS Modules** for styling

---

## 🔑 Example (Fake Auth Flow)

```js
const FAKE_USER = {
  email: "temitope@example.com",
  password: "qwerty",
  name: "Temitope",
};

function login(email, password) {
  if (email === FAKE_USER.email && password === FAKE_USER.password) {
    setUser(FAKE_USER);
  }
}
```

- Correct login → redirects to `/app`.
- Wrong login → stays on login page.
- Logout → clears user and sends back to `/login`.

---

## ⚡ Performance Optimization

- Top-level pages (`Homepage`, `Product`, `Pricing`, `Login`) are **lazy-loaded** using `React.lazy`.
- Nested components (`CityList`, `CountryList`, `City`, `Form`) can also be lazy-loaded to reduce initial bundle size.
- `Suspense` with fallback UI ensures smooth user experience while chunks load.

---

## 📘 My Journey

I learned how React projects are structured in real-world scenarios.

- Struggled at first with **contexts and providers**, but now I can set them up without help.
- Discovered why `navigate("/app", { replace: true })` is important in authentication.
- Learned **Protected Routes** as the “habitat checks” of an application.
- Optimized **performance with lazy-loading**, making the app faster and more scalable.
- Gained confidence to tackle more complex apps and move closer to my frontend developer goals.

---

## 📌 How to Run

1. Clone the repo:

   ```bash
   git clone https://github.com/yourusername/wordwise.git
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Start dev server:

   ```bash
   npm run dev
   ```

---

## 🙌 Acknowledgments

This project was inspired by **Jonas Schmedtmann’s React course**, and I built it while following along the tutorial
