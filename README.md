# Nova Blog Page

## Setup and Instructions

### HTML Structure

> Setting Up the Environment

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Blog Landing Page</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css"
    />
    <style>
      body,
      html {
        height: 100%;
        margin: 0;
      }

      .scroller {
        scroll-behavior: smooth;
      }
    </style>
  </head>
  <body class="flex flex-col h-full bg-gray-100">
    <!-- Navigation -->
    <!-- ... -->
    <!-- Main Content Wrapper -->
    <!-- ... -->
    <!-- Footer -->
    <!-- ... -->
    <script>
      <!-- JavaScript for menu -->
    </script>
  </body>
</html>
```

### Structure Explanation

`Tailwind CSS CDN`: Included via

```html
<script src="https://cdn.tailwindcss.com"></script>
```

`Font Awesome CDN`: Included for icons via

```html
<link
  rel="stylesheet"
  href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css"
/>
```

`Custom CSS`: Applied smooth scrolling to the .scroller class and reset margins and heights.

### HTML for Navigation

> Building the Navigation

```html
<nav class="bg-white shadow-md w-full fixed top-0 z-10">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="flex justify-between h-16">
      <div class="flex">
        <div class="flex-shrink-0 flex items-center">
          <img class="h-8 w-8" src="/path/to/logo.png" alt="Logo" />
          <span class="ml-2 text-xl font-bold">FOOsh</span>
        </div>
        <div class="hidden md:ml-6 md:flex md:space-x-8">
          <a
            href="#one"
            class="border-transparent text-gray-500 hover:text-gray-700 inline-flex items-center px-1 pt-1 text-sm font-medium"
            >About</a
          >
          <a
            href="#four"
            class="border-transparent text-gray-500 hover:text-gray-700 inline-flex items-center px-1 pt-1 text-sm font-medium"
            >Categories</a
          >
        </div>
      </div>
      <div class="flex items-center md:hidden">
        <button
          type="button"
          id="menu-button"
          class="inline-flex items-center justify-center p-2 rounded-md text-gray-400 hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:bg-gray-100 focus:text-gray-500"
          aria-expanded="false"
        >
          <span class="sr-only">Open main menu</span>
          <i id="menu-icon" class="fas fa-bars h-6 w-6"></i>
          <i id="close-icon" class="fas fa-times h-6 w-6 hidden"></i>
        </button>
      </div>
    </div>
  </div>
  <!-- Mobile menu -->
  <div id="mobile-menu" class="md:hidden hidden">
    <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3">
      <a
        href="#one"
        class="block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:text-gray-900 hover:bg-gray-50 menu-item"
        >About</a
      >
      <a
        href="#four"
        class="block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:text-gray-900 hover:bg-gray-50 menu-item"
        >Categories</a
      >
    </div>
  </div>
</nav>
```

### Nav Explanation

Fixed Navigation: The navigation bar is fixed at the top with fixed top-0.
Responsive Design: Flexbox utilities (flex, justify-between, items-center) ensure proper alignment.
Mobile Menu: Hidden by default on larger screens (hidden md:flex) and toggled on smaller screens using JavaScript.

### HTML for Main Content

> Main Content with Smooth Scrolling

```html
<div class="flex-1 mt-16 overflow-y-auto scroller">
  <main class="pt-8">
    <div id="one" class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
        <div class="order-1 md:order-1">
          <img
            class="w-full rounded-lg"
            src="https://imgs.search.brave.com/CLnaRAHKN_hmHd5sPg5TVwRCFVPl8wLm5TAiEF_FHqM/rs:fit:860:0:0:0/g:ce/aHR0cHM6Ly9pbWcu/ZnJlZXBpay5jb20v/ZnJlZS1waG90by9h/aS1nZW5lcmF0ZWQt/bGFicmFkb3ItcmV0/cmlldmVyLWRvZy1w/aWN0dXJlXzIzLTIx/NTA2NDQ5NzYuanBn/P3NpemU9NjI2JmV4/dD1qcGc"
            alt="Bouquet of Fresh Flowers"
          />
        </div>
        <div class="order-2 md:order-2">
          <h2 class="text-3xl font-bold mb-4">
            How to Wrap a Bouquet of Fresh Flowers (and a Secret Freshness
            Trick!)
          </h2>
          <p class="text-gray-700 mb-4">
            Here's how to wrap fresh flowers with a great secret trick to keep
            them fresh with expert Anne...
          </p>
          <p class="text-gray-700">
            Excited to share some of today's tips with our expert florist and
            friend Anne of Flourish CA. Fresh bouquets of flowers you picked up
            at the farmer's market yesterday...
          </p>
        </div>
      </div>
    </div>

    <div id="two" class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
        <div class="order-1 md:order-2">
          <img
            class="w-full rounded-lg"
            src="https://imgs.search.brave.com/CLnaRAHKN_hmHd5sPg5TVwRCFVPl8wLm5TAiEF_FHqM/rs:fit:860:0:0:0/g:ce/aHR0cHM6Ly9pbWcu/ZnJlZXBpay5jb20v/ZnJlZS1waG90by9h/aS1nZW5lcmF0ZWQt/bGFicmFkb3ItcmV0/cmlldmVyLWRvZy1w/aWN0dXJlXzIzLTIx/NTA2NDQ5NzYuanBn/P3NpemU9NjI2JmV4/dD1qcGc"
            alt="Bouquet of Fresh Flowers"
          />
        </div>
        <div class="order-2 md:order-1">
          <h2 class="text-3xl font-bold mb-4">
            How to Wrap a Bouquet of Fresh Flowers (and a Secret Freshness
            Trick!)
          </h2>
          <p class="text-gray-700 mb-4">
            Here's how to wrap fresh flowers with a great secret trick to keep
            them fresh with expert Anne...
          </p>
          <p class="text-gray-700">
            Excited to share some of today's tips with our expert florist and
            friend Anne of Flourish CA. Fresh bouquets of flowers you picked up
            at the farmer's market yesterday...
          </p>
        </div>
      </div>
    </div>
  </main>
</div>
```

### HTML Explanation

Smooth Scrolling: Applied scroll-behavior: smooth to the .scroller class.
Responsive Grid: Used Tailwind’s grid utilities (grid, grid-cols-1, md:grid-cols-2) to create a responsive layout.
Content Order: Controlled the order of content using order-1, md:order-1, etc.

## HTML for Footer

> Footer

```html
<footer class="bg-white py-6">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="flex justify-between">
      <div>
        <h3 class="text-lg font-bold">Useful Links</h3>
        <ul class="mt-2 space-y-2">
          <li>
            <a href="#" class="text-gray-600 hover:text-gray-900"
              >Privacy Policy</a
            >
          </li>
        </ul>
      </div>
      <div>
        <h3 class="text-lg font-bold">Follow Us</h3>
        <ul class="mt-2 space-y-2">
          <li>
            <a href="#" class="text-gray-600 hover:text-gray-900">Facebook</a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</footer>
```

### Footer Explanation

Footer Layout: Used Flexbox utilities (flex, justify-between) for layout.
Spacing: Applied padding and margin utilities (py-6, mt-2, space-y-2) for spacing.

## JavaScript for Toggling Menu

> JavaScript for Mobile Menu

```html
<script>
  const menuButton = document.getElementById("menu-button");
  const mobileMenu = document.getElementById("mobile-menu");
  const menuIcon = document.getElementById("menu-icon");
  const closeIcon = document.getElementById("close-icon");
  const menuItems = document.querySelectorAll(".menu-item");

  menuButton.addEventListener("click", () => {
    const expanded =
      menuButton.getAttribute("aria-expanded") === "true" || false;
    menuButton.setAttribute("aria-expanded", !expanded);
    mobileMenu.classList.toggle("hidden");
    menuIcon.classList.toggle("hidden");
    closeIcon.classList.toggle("hidden");
  });

  menuItems.forEach((item) => {
    item.addEventListener("click", () => {
      mobileMenu.classList.add("hidden");
      menuIcon.classList.remove("hidden");
      closeIcon.classList.add("hidden");
      menuButton.setAttribute("aria-expanded", false);
    });
  });
</script>
```

### JS Explanation

Toggle Menu: JavaScript to toggle the visibility of the mobile menu and icons (`menu-icon`, `close-icon`).
Event Listeners: Added event listeners to handle clicks on the menu button and menu items.
Key Takeaways for Tailwind CSS Beginners
Utility-First Approach: Tailwind CSS is a utility-first CSS framework, meaning you use predefined classes to style elements directly in your HTML.
Responsive Design: Tailwind’s responsive utility variants (e.g., `md:grid-cols-2`, `sm:px-6`) allow for easy creation of responsive layouts.
Flexbox and Grid: Tailwind provides a comprehensive set of Flexbox and Grid utilities for creating complex layouts.
Customization: Tailwind classes can be combined and customized to fit your design needs without writing custom CSS.
Utility Classes: Learn and leverage the extensive set of utility classes for margins, padding, colors, typography, and more.
By following these steps and understanding the provided explanations, you should be able to build and customize a Tailwind CSS layout effectively.
