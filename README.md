# ?? Shopping Cart - React & `useReducer` + Context API

A feature-rich, responsive Shopping Cart application built with **React**, **Vite**, **Context API**, and the **`useReducer`** hook for clean, centralized global state management.

---

## ?? Key Features

- ??? **Product Listing**: Browse available products with images, titles, prices, and descriptions.
- ? **Add to Cart**: Easily add products to the cart with toast notifications (`react-toastify`).
- ?? **Quantity Controls**: Dynamically increase or decrease item quantities in real time.
- ??? **Item Removal**: Remove individual items from the cart.
- ?? **Total Price Calculation**: Automatically calculates the cart subtotal based on item quantities and prices.
- ?? **Interactive Cart Modal**: Overlay drawer/modal for viewing items and managing cart operations cleanly.
- ?? **Modular Styling**: Scoped styling using CSS Modules (`.module.css`) to avoid class collisions.
- ?? **Custom `useCart` Hook**: Simplified context consumption throughout component hierarchy.

---

## ??? Project Architecture & State Management

The application demonstrates best practices in managing global state without third-party state management libraries like Redux:

### 1. `useReducer` Reducer Actions (`CartProvider.jsx`)
- `ADD_ITEM`: Adds a new item to the cart array.
- `INCREASE_ITEM`: Increments the quantity of a specific cart item.
- `DECREASE_ITEM`: Decrements the quantity of a specific cart item.
- `REMOVE_ITEM`: Filters out an item from the cart by its unique `id`.

### 2. Context API Integration
The `CartProvider` component wraps the app, exposing the cart state and helper functions (`addItemsCart`, `increaseQty`, `decreaseQty`, `removeItemFromCart`) via context. A custom hook `useCart()` is exported to streamline access across components.

---

## ?? Project Structure

```
shopping-cart/
+-- public/
¦   +-- vite.svg
+-- src/
¦   +-- components/
¦   ¦   +-- UI/
¦   ¦   ¦   +-- Container.jsx
¦   ¦   ¦   +-- Container.module.css
¦   ¦   ¦   +-- Modal.jsx
¦   ¦   ¦   +-- Modal.module.css
¦   ¦   +-- Cart.jsx
¦   ¦   +-- Cart.module.css
¦   ¦   +-- CartItem.jsx
¦   ¦   +-- CartItem.module.css
¦   ¦   +-- Header.jsx
¦   ¦   +-- Header.module.css
¦   ¦   +-- Product.jsx
¦   ¦   +-- Product.module.css
¦   ¦   +-- Products.jsx
¦   ¦   +-- Products.module.css
¦   +-- contexts/
¦   ¦   +-- CartProvider.jsx
¦   +-- data/
¦   ¦   +-- productsData.js
¦   +-- App.css
¦   +-- App.jsx
¦   +-- index.css
¦   +-- main.jsx
+-- package.json
+-- vite.config.js
+-- README.md
```

---

## ??? Tech Stack & Dependencies

- **Frontend Framework**: [React 18](https://react.dev/)
- **Build Tool**: [Vite](https://vitejs.dev/)
- **Icons**: [React Icons](https://react-icons.github.io/react-icons/)
- **Toast Notifications**: [React Toastify](https://fkhadra.github.io/react-toastify/introduction/)
- **Styling**: CSS Modules & Vanilla CSS

---

## ?? Getting Started

Follow these steps to set up and run the project locally on your machine:

### 1. Clone the Repository
```bash
git clone https://github.com/Tausifqureshi/ShopingCard_React_useReducer.git
cd ShopingCard_React_useReducer
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Run Development Server
```bash
npm run dev
```
Open [http://localhost:5173](http://localhost:5173) in your browser to view the application.

---

## ?? Available Scripts

- `npm run dev` - Launches the Vite development server.
- `npm run build` - Builds the application for production.
- `npm run preview` - Locally previews the production build.
- `npm run lint` - Runs ESLint to check for code quality.

---

## ?? Author

Created by [Tausif Qureshi](https://github.com/Tausifqureshi).
