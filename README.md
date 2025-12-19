# PlacePicker – React Side Effects & `useEffect` 🌍⚛️

This project is my practice app for the **Side Effects & `useEffect`** section of  
Maximilian Schwarzmüller’s *React – The Complete Guide (incl. Redux)* on Udemy.

The app is called **PlacePicker** and is centered around picking vacation spots while
reacting to browser APIs and other side effects in a controlled way via `useEffect`.

---

## 🧠 What are “side effects”?

In React, a **side effect** is anything that touches the outside world
beyond pure rendering, for example:

- Fetching or storing data (APIs, `localStorage`, etc.)
- Using browser APIs (like **geolocation**)
- Setting up timers or subscriptions
- Manually interacting with the DOM

`useEffect` lets us run this kind of logic **after** React updates the UI and
only when specific dependencies change, instead of on every render.

---

## 🎯 Project goals

- Practice recognizing **side effects** and keeping them out of pure render logic
- Use **`useEffect`** to:
  - Run code on mount / dependency changes
  - Control when effects re-run with the **dependency array**
  - Clean up when components unmount or dependencies change
- Integrate browser features (like **geolocation**) in a React-friendly way
- Coordinate **modals and other UI state** with side-effectful logic

---

## 🧩 Concepts practiced in PlacePicker

### 1. Geolocation with `useEffect`

- Requesting the user’s location when the app loads or when certain state changes
- Storing coordinates in React state
- Making sure the geolocation request is issued from inside an effect
  instead of directly in the render phase

### 2. Modals & UI side effects

- Showing and hiding modals based on state
- Using `useEffect` to react when a particular value changes
  (for example, when a place is selected or a result is ready)
- Cleaning up any timers or listeners when the modal closes or the
  component unmounts

### 3. Dependency arrays

- Running an effect **once** on mount with `useEffect(..., [])`
- Re-running effects when specific values change with `useEffect(..., [value])`
- Avoiding effects that re-run on every render without need

### 4. Cleanup functions

- Returning a cleanup function from `useEffect` when an effect:
  - Subscribes to something
  - Registers a listener
  - Starts a timer
- Ensuring that subscriptions and timers are cleared to prevent memory leaks
  and inconsistent behavior

---

## 🚀 Getting started

```bash
git clone https://github.com/premanpatel/react-useeffect.git
cd react-useeffect
npm install
npm start
```

---

Then open your browser at `http://localhost:3000` (or whatever URL your dev setup prints).

> This project assumes a standard React dev setup (Create React App / Vite style).  
> If you see dependency warnings, run `npm install` again or delete `node_modules` and reinstall.

---

## 🏷️ Attribution

Course: *React – The Complete Guide (incl. Redux)* by Academind / Maximilian Schwarzmüller on Udemy.  
This repo contains **my own practice code** and experiments based on that course; it does **not** include the original course materials.
