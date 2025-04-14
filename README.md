# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
Make the webpage responsive using media queries.
Ensure proper alignment and spacing.

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.

Happy Coding! 💻✨

https://codepen.io/jummy001/pen/MYWMKyY
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Responsive Layout with Flexbox & Grid</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <!-- Navigation Bar -->
  <header class="navbar">
    <nav>
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#aside">About</a></li>
        <li><a href="#">Services</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>
  </header>

  <!-- Main Content Layout with Grid -->
  <main class="container">
    <section class="sidebar">
      <h2>Sidebar</h2>
      <p>Fashion has always been a part of men’s and women’s lives. That’s why we see a lot of fashion brands that provide various fashion clothing, accessories, and other products to both men and women. Rino-Pelle brings luxurious and contemporary fashion items for wearable prices to enable every woman to achieve that effortlessly chic lifestyle. Being part of these fashion website designs, its website is packed with enticing features worth exploring.</p>
    </section>

    <section class="content">
      <h1>Welcome to My Webpage</h1>
      <p>it’s a unique program that crafts sneakers perfectly fitted to the wearer from the start and grows more personalized over time. The website’s layout comprises overlapping scrolling sections, animated typography, product blueprints, a presentation video, and seamlessly integrated social media posts. It embraces vibrant colors like purple, green, and orange gradients.</p>
    </section>

    <section class="aside">
      <h2>Additional Info</h2>
      <pA top-notch Shopify theme designed exclusively for upscale jewelry stores, crafted to showcase the quality and artistry of your products while offering ample opportunities for brand storytelling.

Arda is packed with effective features to help turn visitors into buyers. From captivating animations to useful tools like image hotspots, product options, and advanced search, Arda equips you with everything you need to boost sales</p>
    </section>
  </main>

  <!-- Footer -->
  <footer class="footer">
    <p>© 2025 My Webpage. All rights reserved.</p>
  </footer>
</body>
</html>

/* Reset basic margins and padding */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
   scroll-behavior: smooth;
}

/* Body styles */
body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  background-color: pink;
  color: #333;
}

/* Navigation Bar using Flexbox */
.navbar {
  background-color: #007acc;
  padding: 10px 20px;
}

.navbar nav ul {
  display: flex;
  justify-content: space-around;
  list-style: none;
}

.navbar nav ul li {
  margin: 0 10px;
}

.navbar nav ul li a {
  color: white;
  text-decoration: none;
  font-size: 1.1em;
}

.navbar nav ul li a:hover {
  text-decoration: underline;
}

/* Grid Layout for Main Content */
.container {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;
  gap: 20px;
  padding: 20px;
}

/* Sidebar, Content, Aside Sections */
.sidebar, .content, .aside {
  background-color: black;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.sidebar, .aside {
  background-color: #e1e1e1;
}

.content {
  background-color: #fff;
  grid-column: span 2;
}

/* Footer */
.footer {
  background-color: #007acc;
  color: white;
  padding: 20px;
  text-align: center;
  margin-top: 20px;
}

/* Media Queries for Responsiveness */

/* Mobile view (up to 600px) */
@media (max-width: 600px) {
  .navbar nav ul {
    flex-direction: column;
    align-items: center;
  }

  .container {
    grid-template-columns: 1fr;
  }

  .content {
    grid-column: span 1;
  }
}

/* Tablet view (601px to 900px) */
@media (min-width: 601px) and (max-width: 900px) {
  .navbar nav ul {
    justify-content: center;
  }

  .container {
    grid-template-columns: 1fr 2fr;
  }
}

/* Desktop view (above 900px) */
@media (min-width: 901px) {
  .container {
    grid-template-columns: 1fr 2fr 1fr;
  }
}

