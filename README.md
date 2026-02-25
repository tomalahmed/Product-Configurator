# 📦 Pure CSS Product Configurator

A fully interactive product configurator built entirely with **HTML & CSS — no JavaScript**.
This project demonstrates how to handle UI state, theming, and interactivity using pure CSS techniques such as hidden radio inputs (Checkbox Hack), CSS variables, and sibling combinators.

---

## 🚀 Features

* **Zero JavaScript** — all logic powered by CSS
* **State Management** via hidden `<input type="radio">`
* **Dynamic Theming** using CSS custom properties
* **Responsive Design** with smooth transitions
* Clean, modern product card UI

---

## 🛠️ How It Works

### State Management

Hidden radio inputs are used to track the selected theme.

```html
<input type="radio" name="color" id="clr-red" checked>
<input type="radio" name="color" id="clr-blue">
<!-- add more colors here -->
```

By placing these inputs at the top of the DOM, later CSS selectors can react when a specific radio is checked.

### Theming Logic

When a color input is checked, custom CSS properties are updated:

```css
#clr-blue:checked ~ .main-container {
    --theme-color: #0984e3;
    --theme-shadow: rgba(9, 132, 227, 0.4);
}
```

This changes the theme of the app instantly, including highlights, shadows, and primary UI colors.

---

## 🎨 Interactivity

The visible color swatches are `<label>` elements linked to the hidden radios. Clicking a swatch checks the corresponding radio input, which triggers the CSS state change.

```html
<label for="clr-red" class="color-swatch red"></label>
```

---

## 📦 Getting Started

1. **Clone the repository**

   ```bash
   git clone https://github.com/tomalahmed/Product-Configurator.git
   ```
2. **Open** `index.html` in a browser
3. **Click a color swatch** to update the theme instantly

---

## 🧩 Adding New Colors

To add a new color theme:

### 1. HTML

Add a new radio input:

```html
<input type="radio" name="color" id="clr-green">
```

Add a color swatch label:

```html
<label for="clr-green" class="color-swatch green"></label>
```

### 2. CSS

Define theme variables for the new color:

```css
#clr-green:checked ~ .main-container {
    --theme-color: #00b894;
    --theme-shadow: rgba(0, 184, 148, 0.4);
}
```

That’s it! Your new theme will work automatically.

---

## 🧠 What You’ll Learn

* Creative CSS state management without JavaScript
* Using radio inputs and sibling selectors for interactivity
* Modifying CSS variables dynamically
* Building responsive UI components with modern CSS

---

## 💡 Why It Matters

This project proves you can build **complex UI interactions and stateful behavior using only CSS** — no frameworks or scripting required. It’s lightweight, hack-free, and works in all modern browsers.

---

## 📌 License

MIT © tomalahmed
