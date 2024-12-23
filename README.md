# VaibhavEcomm

## Building an E-Commerce Website with Vanilla JavaScript

This project is a simple e-commerce website built using Vanilla JavaScript, designed for dynamic interactions and smooth user experiences. The project utilizes a structured folder system, modular JavaScript functions, and Vite for efficient development and builds.

---

### Folder Structure

#### Option 1:
```
my-vanilla-js-project/
├── public/
│   ├── images/
│   │   ├── logo.png
│   │   └── background.jpg
│   └── index.html
├── src/
│   ├── index.html
│   ├── main.js
│   ├── utils.js
│   └── styles.css
├── vite.config.js
└── package.json
```

#### Option 2:
```
my-vanilla-js-project/
├── public/
│   ├── images/
│   │   ├── logo.png
│   │   └── background.jpg
│   └── index.html
├── index.html
├── main.js
├── styles.css
├── vite.config.js
└── package.json
```

---

### Key Functionalities

#### Displaying Product Containers

1. **Selecting DOM Elements**: Use `document.querySelector()` to select elements for the product container and template container.
2. **Defining the Function**: Create a `showProductContainer` function that accepts an array of products.
3. **Valid Input Check**: Ensure the `products` array is valid; return `false` if invalid.
4. **Iterating Over Products**: Use `forEach()` to loop through the array.
5. **Destructuring Properties**: Destructure properties like `brand`, `category`, `description` for readability.
6. **Cloning Templates**: Use `document.importNode()` to clone templates for each product.
7. **Updating Information**: Populate product details and calculate/display prices dynamically.
8. **Adding Event Listeners**: Handle click events using event delegation for elements like `.stockElement`.
9. **Appending to Container**: Append updated templates to the product container.
10. **Container Availability Check**: Ensure the container exists before appending.

#### Quantity Management with `homeQuantityToggle`

1. Create a new file `quantityToggle.js`.
2. Define `homeQuantityToggle(event, id, stock)`.
3. Select card elements and retrieve/update product quantity and attributes.
4. Handle increment and decrement events based on stock and current quantity.
5. Return the updated quantity.

#### Add to Cart Functionality

1. Select the product card and retrieve its price and quantity.
2. Use `getCartProductFromLocalStorage` to retrieve existing cart data.
3. Calculate the total price and update the cart in local storage.
4. Handle duplicate values to prevent redundant entries.

#### Retrieve and Update Cart

1. Retrieve cart products using `localStorage.getItem()` and parse them.
2. Display cart products dynamically by cloning templates and appending to the cart container.
3. Update the cart value on page load and after any changes.

#### Cart Item Management

1. Use `removeTheCardFromCart` to delete items and update local storage.
2. Implement `incrementDecrement` to adjust product quantities in the cart dynamically.
3. Update the total cart price with `updateCartProductTotal`, ensuring correct subtotal and order total.

---

### Extra Information on Vite

#### Configuration

1. Import `defineConfig` from Vite and `resolve` from Node.js’s `path` module.
2. Use the `build` property to configure Rollup options for multiple entry points.
3. Use `__dirname` for relative paths to ensure compatibility.

Example `vite.config.js`:
```javascript
import { defineConfig } from 'vite';
import { resolve } from 'path';

export default defineConfig({
  build: {
    rollupOptions: {
      input: {
        main: resolve(__dirname, 'index.html'),
      },
    },
  },
});
```

---

### How to Run the Project

1. Clone the repository:
   ```bash
   git clone <repository-url>
   ```

2. Navigate to the project directory:
   ```bash
   cd my-vanilla-js-project
   ```

3. Install dependencies:
   ```bash
   npm install
   ```

4. Start the development server:
   ```bash
   npm run dev
   ```

5. Build the project for production:
   ```bash
   npm run build
   ```

6. Preview the production build:
   ```bash
   npm run preview
   ```

---

### Conclusion

This project demonstrates how to build a fully functional e-commerce platform with Vanilla JavaScript. By following the outlined steps and leveraging modular JavaScript, dynamic DOM manipulation, and efficient development tools like Vite, you can create a scalable and maintainable web application. Happy coding!

