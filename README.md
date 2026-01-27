# Pure CSS Product Configurator

A highly interactive product configurator built entirely with HTML and CSS Only. No JavaScript.
This project demonstrates how to handle state management, theming, and interactivity using advanced CSS techniques like the "Checkbox Hack" (using hidden radio buttons and sibling combinators).

Project Preview! - https://tomalahmed.github.io/Product-Configurator

## 🚀 Features

-   **Zero JavaScript**: All logic is handled via CSS.
-   **State Management**: Uses hidden `<input type="radio">` elements to track selected colors.
-   **Dynamic Theming**: CSS Variables (`--theme-color`, `--bg-color`) update instantly based on selection.
-   **Smooth Animations**: Transitions for colors, shadows, and transform effects.
-   **Responsive Design**: Clean and modern card layout.

## 🛠️ How It Works

The core logic relies on the **General Sibling Combinator (`~`)** and **CSS Variables**.

1.  **HTML Structure**: Radio buttons are placed at the very top of the DOM, before the main content.
    ```html
    <input type="radio" name="color" id="clr-red" checked>
    <input type="radio" name="color" id="clr-blue">
    <!-- ... -->
    <div class="main-container">...</div>
    ```

2.  **CSS Logic**: When a specific radio is checked, we override CSS variables for the content that follows it.
    ```css
    #clr-blue:checked ~ .main-container {
        --theme-color: #0984e3;
        --theme-shadow: rgba(9, 132, 227, 0.4);
    }
    ```

3.  **Interactivity**: The color swatches inside the card are actually `<label>` elements linked to the hidden radio buttons. Clicking a label checks the corresponding radio button, triggering the CSS state change.

## 📦 Usage

1.  Clone the repository or download the files.
2.  Open `index.html` in any modern web browser.
3.  Click the color swatches to see the theme change instantly.

## 🎨 Customization

To add a new color:

1.  **HTML**: Add a new `<input>` at the top and a `<label>` in the `.color-picker` section.
2.  **CSS**: Add a new rule block in `styles.css`:
    ```css
    #clr-newcolor:checked ~ .main-container {
        --theme-color: #your-color-code;
        /* ... other variables */
    }
    ```
#Done with Love.
