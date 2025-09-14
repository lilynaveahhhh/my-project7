# 🛍️ ProductCard Component Using Props

## 📌 Title
ProductCard Component Using Props

## 🎯 Objective
Build a reusable React component that displays product details using **props**.  
This task helps you understand how to **pass and render dynamic data** in React components.

---

## 📖 Task Description
- Create a React component named **`ProductCard`**.  
- It should accept the following **props**:
  - `name` → Product name
  - `price` → Product price
  - `inStock` → Stock status (true/false or string)  
- The component should display all three details clearly (e.g., inside a card layout).  
- Demonstrate how **different product data** can be passed into the component and rendered dynamically without changing the component code.

---

## 🏗️ Example Code

### `ProductCard.jsx`
```jsx
import React from "react";

function ProductCard({ name, price, inStock }) {
  return (
    <div style={styles.card}>
      <h2>{name}</h2>
      <p>💰 Price: ${price}</p>
      <p>
        {inStock ? (
          <span style={{ color: "green" }}>✅ In Stock</span>
        ) : (
          <span style={{ color: "red" }}>❌ Out of Stock</span>
        )}
      </p>
    </div>
  );
}

const styles = {
  card: {
    border: "1px solid #ccc",
    borderRadius: "10px",
    padding: "16px",
    margin: "10px",
    width: "250px",
    textAlign: "center",
    boxShadow: "0 2px 6px rgba(0,0,0,0.1)",
  },
};

export default ProductCard;
