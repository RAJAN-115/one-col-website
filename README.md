# One Column Website Layout - Brief Documentation



## **Key Concepts and Workflow**
1. **Project Setup**
   - Folder structure: `index.html`, `styles.css`, `images/`
   - Including Google Fonts and favicon

2. **HTML Skeleton**
   - `<header>`: logo and main navigation menu
   - `<section>` elements: introduction, features, services
   - `<aside>`: sidebar widget area
   - `<article>`: detailed content blocks
   - `<footer>`: contact info and social links

3. **CSS Layout Techniques**
   - **Box Model** fundamentals: `margin`, `padding`, `border`
   - **Centering container**: `max-width: 960px; margin: 0 auto;`
   - **Clearfix**: `.clearfix::after { content: ""; display: table; clear: both; }`
   - **Floats**: `.sidebar { float: right; width: 30%; }` and `.content { float: left; width: 70%; }`
   - **Positioning**: relative and absolute for overlays

4. **Responsive Design Enhancements**
   - Mobile-first approach: base styles then `@media (min-width:768px)` adjustments
   - Flexible images: `img { max-width: 100%; height: auto; }`
   - Navigation toggle: hamburger menu with CSS and minimal JavaScript

5. **Enhancements and Best Practices**
   - Semantic HTML5 elements for accessibility
   - Externalizing styles and scripts
   - Performance: minifying CSS, using sprites

## **Practice Code Snippets**

### HTML (index.html)
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>One Column Website</title>
  <link href="https://fonts.googleapis.com/css?family=Open+Sans&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header class="clearfix">
    <h1 class="logo">MySite</h1>
    <nav>
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#services">Services</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>
  <section class="intro">
    <h2>Welcome to MySite</h2>
    <p>Introduction paragraph with overview.</p>
  </section>
  <div class="main clearfix">
    <article class="content">
      <h3>Our Services</h3>
      <p>Details about services offered.</p>
    </article>
    <aside class="sidebar">
      <h4>Quick Links</h4>
      <ul>
        <li><a href="#">Blog</a></li>
        <li><a href="#">Portfolio</a></li>
      </ul>
    </aside>
  </div>
  <footer>
    <p>&copy; 2025 MySite | <a href="#contact">Contact Us</a></p>
  </footer>
</body>
</html>
```

### CSS (styles.css)
```css
* { box-sizing: border-box; margin: 0; padding: 0; }
body { font-family: 'Open Sans', sans-serif; }
.clearfix::after { content: ""; display: table; clear: both; }
header { background: #333; color: #fff; padding: 20px; }
.logo { float: left; }
nav ul { float: right; list-style: none; }
nav ul li { display: inline; margin-left: 15px; }
a { color: #fff; text-decoration: none; }
.intro { padding: 40px 20px; background: #f4f4f4; text-align: center; }
.main { padding: 20px; }
.content { float: left; width: 70%; }
.sidebar { float: right; width: 30%; background: #eaeaea; padding: 20px; }
footer { background: #333; color: #fff; text-align: center; padding: 15px; }
img { max-width: 100%; height: auto; }
@media (max-width: 768px) {
  .content, .sidebar { float: none; width: 100%; }
  nav ul li { display: block; margin: 10px 0; }
}
```

## **24-Hour Action Steps**
1. **Build the Project Structure** (1 hour): Create folders and files, link CSS and assets
2. **Implement Layout** (2 hours): Code HTML and CSS, test floats and clearfix behavior
3. **Add Responsive Features** (1 hour): Apply media queries and test on various devices

## **Challenge Questions**
1. How does the **clearfix technique** resolve float containment issues?
2. What are the pros and cons of using **float-based layouts** versus **Flexbox** or **Grid**?
3. How would you implement a **sticky header** for this one-column layout?
