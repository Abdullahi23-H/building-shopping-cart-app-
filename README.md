Desserts E-Commerce: Logic-First Shopping Cart
A specialized shopping cart application built with a focus on Object-Oriented Programming (OOP) and clean state management. This project moves beyond simple scripting by encapsulating complex retail logic within a robust JavaScript Class architecture.

🚀 Key Engineering Features
1. Class-Based Architecture (ShoppingCart)
I chose to encapsulate the cart logic within a ShoppingCart class. This ensures:

State Integrity: All cart data (items, total, taxRate) is contained in one source of truth.

Method Reusability: Logic for tax calculations and totals are modular methods, making the code easier to scale.

2. Mastering Execution Context (this)
A technical highlight of this project was managing the execution context in JavaScript. When passing a class method to an event listener, the function "loses" its connection to the object. I solved this by using Explicit Binding to ensure the clearCart method maintains access to the class instance.

JavaScript

// The "Glue" that connects the UI to the Logic
clearCartBtn.addEventListener("click", cart.clearCart.bind(cart));
3. Real-Time Data Processing & Optimized DOM
To keep the UI performant, I implemented logic that differentiates between adding a new product to the view and simply updating the quantity of an existing one. This prevents unnecessary DOM re-renders.

JavaScript

// Logic to toggle between 'new item' and 'increment quantity'
currentProductCount > 1 
  ? currentProductCountSpan.textContent = `${currentProductCount}x`
  : productsContainer.innerHTML += `<div id="dessert${id}" class="product">...</div>`;
🛠️ Technical Stack
Frontend: Semantic HTML5, CSS3 (Flexbox/Grid)

Logic: JavaScript ES6+ (Classes, Array Methods, Template Literals)

Design: Responsive UI with CSS Variables for theme consistency.

🧠 What I Learned
During this build, I deep-dived into how the JavaScript engine handles the Execution Context. Solving the "disappearing this" problem reinforced my understanding of how memory and scope work under the hood. I also utilized the .reduce() method for price calculations, ensuring high performance even as the item list grows.

📬 Connect with me
If you're interested in clean, scalable JavaScript architecture, let's chat!

[abdullahi mahad] [https://abdullahiportfolio.com/Linkedin.com/in/abdullahi-mahad-a05552373]
