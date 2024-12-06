---
layout: essay
type: essay
title: "From Weather Apps to Shoppings Carts"
# All dates must be YYYY-MM-DD format!
date: 2024-12-05
published: true
labels:
  - Design Patterns 
  - Growth
  - 3 Snippts of Code
---


-------------------------------------------

## From a Weather App to a Shopping Cart

In software development, just like in any field, there are proven ways of solving problems. These methods are called design patterns. Think of them as best practices or blueprints that developers use to make their code work better, be more organized, and easier to manage. This essay will explain what design patterns are and demonstrate how they appear in three different code examples. By the end, we’ll answer two questions: What are design patterns? and What design patterns have been used in the code examples?


## What Are Design Patterns?

A design pattern is a general solution to a common problem that developers face when writing software. It's not a specific piece of code, but more of a guide that shows how to solve a problem in a structured way. Imagine you have a problem, and instead of coming up with a brand new solution from scratch, you follow a recipe that has worked for others in similar situations. That's what design patterns do for developers—they offer proven solutions that can be adapted to different situations.

Design Patters can be divided into three main types:

1. Creational Patterns: These focus on how objects are created in a program.

2. Structural Patterns: These deal with how different parts of a program are organized or connected.

3. Behavioral Patterns: These describe how objects interact and communicate with each other.


## A Simple Weather Function – Strategy Pattern

The first code snippet is a function that calculates the "feels like" temperature based on the temperature and humidity. It then provides a "danger level" based on how hot and humid it is. This function makes use of a strategy pattern.

The strategy pattern is a way of allowing a program to choose from different methods of doing something, depending on the situation. It lets you change the approach or behavior at runtime.

In this case, the function calculates the "feels like" temperature using a formula, and depending on that value, it categorizes the result into different danger levels (Extreme Danger, Danger, Caution, etc.). While the function doesn't explicitly switch between different strategies (formulas), the idea of using different thresholds to categorize the temperature is similar to the strategy pattern.
 

```
function feelsLike(temp: number, humidity: number): string {
    const feels = -42.379 + (2.049 * temp) + (10.143 * humidity) - ...;
    let dangerLevel: string;

    if (feels >= 125) {
        dangerLevel = "Extreme Danger";
    } else if (feels >= 102) {
        dangerLevel = "Danger";
    } else if (feels >= 90) {
        dangerLevel = "Extreme Caution";
    } else if (feels >= 79) {
        dangerLevel = "Caution";
    } else {
        dangerLevel = "OK";
    }

    return `feels like ${feels.toFixed(2)}: ${dangerLevel}`;
}

```

This function is using "if-else" statements to decide what category the calculated temperature should fall into. If we wanted to make it more flexible, we could use different formulas (strategies) based on things like the season or user preferences, which is where the strategy pattern would really shine.


## Header Component – Composite Pattern

The second code snippet is a React component that displays the header of a website. This header contains several smaller parts, like the restaurant's name, navigation links, and social media links. The structure of this component is a good example of the composite pattern.

The composite pattern is a way to organize components or objects into a tree-like structure, where both individual components and groups of components can be treated the same way. It’s especially useful when you have objects that can be grouped together and you want to treat them as a whole.

In this case, the header itself is a composite made of smaller parts (the restaurant's name, navigation links, dropdown menus, etc.). Even though these parts are separate, they are grouped together as a single "header" component, making it easier to manage.

```
const Header = () => (
  <div className="container-fluid">
    <header id="header" className="d-flex justify-content-between align-items-center px-3">
      <div id="dyn_logo" className="h4 text-white">
        Jade Dynasty Seafood Restaurant
      </div>
      <nav className="navbar navbar-expand-lg navbar-light">
        <button className="navbar-toggler">...</button>
        <div className="collapse navbar-collapse" id="navbarNav">
          <ul className="navbar-nav">
            <li className="nav-item">
              <Link href="/" className="nav-link">Home</Link>
            </li>
            <li className="nav-item">
              <Link href="/about" className="nav-link">About</Link>
            </li>
            <li className="nav-item">
              <Link href="/press" className="nav-link">Press</Link>
            </li>
            <li className="nav-item dropdown">...</li>
          </ul>
        </div>
      </nav>
    </header>
  </div>
);

```

Here, the Header component combines different smaller components into one big component. The menu items (Home, About, Press) and the logo are treated as individual parts but are grouped together to form the full header. This is exactly what the composite pattern is all about—combining simple parts into a more complex whole, making it easier to manage and render.


## Shopping Cart – Observer Pattern

The third code snippet is a React component that displays a shopping cart. This component listens for changes in the cart and updates the UI accordingly when items are added or removed. This is a good example of the observer pattern.

The observer pattern is a way of letting one part of a program notify other parts when something changes. In this case, when an item is added or removed from the shopping cart, the cart component "wakes up" and updates the display to reflect the change.

```
const CartPage = () => {
  const [cartItems, setCartItems] = useState<ProjectCardData[]>([]);
  const [isClient, setIsClient] = useState(false);

  useEffect(() => {
    setIsClient(true);
    const cart = JSON.parse(localStorage.getItem('cart') || '[]');
    setCartItems(cart);

    const updateCart = () => {
      const updatedCart = JSON.parse(localStorage.getItem('cart') || '[]');
      setCartItems(updatedCart);
    };

    window.addEventListener('cartUpdated', updateCart);

    return () => {
      window.removeEventListener('cartUpdated', updateCart);
    };
  }, []);
}
```

In this example, the component listens for changes in the shopping cart by waiting for an event (cartUpdated). When the cart is updated, it triggers an update to the component’s state and re-renders the UI. This is a direct application of the observer pattern, where the component "observes" changes in the cart and reacts accordingly.

## The Value of Design Patterns
Design patterns are powerful tools in software development because they help solve common problems in a structured and efficient way. In the examples we looked at:

1. The strategy pattern was used in the weather function to categorize the "feels like" temperature.

2. The composite pattern was used in the header component to organize different parts of the page into a cohesive whole.

3. The observer pattern was used in the shopping cart to automatically update the UI when the cart changes.

By using these design patterns, developers can write code that is more flexible, maintainable, and easier to understand. Rather than reinventing the wheel for each new project, design patterns let developers build on established solutions that have already been tested and proven effective. This leads to faster development, fewer bugs, and better software overall.
