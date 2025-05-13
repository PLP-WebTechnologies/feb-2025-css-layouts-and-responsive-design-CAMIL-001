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


# HTML (index.html)
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Layout Demo</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <div class="logo">Logo</div>
        <nav class="navbar">
            <ul class="nav-links">
                <li><a href="#">Home</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Services</a></li>
                <li><a href="#">Portfolio</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
            <div class="burger">
                <div class="line1"></div>
                <div class="line2"></div>
                <div class="line3"></div>
            </div>
        </nav>
    </header>

    <main class="container">
        <section class="hero">
            <h1>Welcome to Our Website</h1>
            <p>Discover amazing products and services</p>
            <button class="cta-button">Learn More</button>
        </section>

        <section class="features">
            <article class="feature-card">
                <h2>Feature One</h2>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
            </article>
            <article class="feature-card">
                <h2>Feature Two</h2>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
            </article>
            <article class="feature-card">
                <h2>Feature Three</h2>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
            </article>
        </section>

        <section class="gallery">
            <div class="gallery-item">1</div>
            <div class="gallery-item">2</div>
            <div class="gallery-item">3</div>
            <div class="gallery-item">4</div>
            <div class="gallery-item">5</div>
            <div class="gallery-item">6</div>
        </section>
    </main>

    <footer>
        <div class="footer-content">
            <div class="footer-section">
                <h3>About Us</h3>
                <p>Company information and mission statement.</p>
            </div>
            <div class="footer-section">
                <h3>Quick Links</h3>
                <ul>
                    <li><a href="#">Home</a></li>
                    <li><a href="#">Services</a></li>
                    <li><a href="#">Contact</a></li>
                </ul>
            </div>
            <div class="footer-section">
                <h3>Contact Info</h3>
                <p>Email: info@example.com</p>
                <p>Phone: (123) 456-7890</p>
            </div>
        </div>
        <div class="footer-bottom">
            &copy; 2023 Your Company. All rights reserved.
        </div>
    </footer>

    <script src="script.js"></script>
</body>
</html>

# CSS (style.css)
/* Base Styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    line-height: 1.6;
    color: #333;
}

header {
    background-color: #2c3e50;
    color: white;
    padding: 1rem;
    position: sticky;
    top: 0;
    z-index: 100;
}

.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 1rem;
}

/* Navigation - Flexbox */
.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.nav-links {
    display: flex;
    list-style: none;
}

.nav-links li {
    margin-left: 2rem;
}

.nav-links a {
    color: white;
    text-decoration: none;
    font-weight: 500;
    transition: color 0.3s;
}

.nav-links a:hover {
    color: #3498db;
}

.burger {
    display: none;
    cursor: pointer;
}

.burger div {
    width: 25px;
    height: 3px;
    background-color: white;
    margin: 5px;
    transition: all 0.3s ease;
}

/* Hero Section */
.hero {
    background-color: #3498db;
    color: white;
    padding: 4rem 2rem;
    text-align: center;
    margin-bottom: 2rem;
    border-radius: 8px;
}

.hero h1 {
    font-size: 2.5rem;
    margin-bottom: 1rem;
}

.cta-button {
    background-color: #2c3e50;
    color: white;
    border: none;
    padding: 0.8rem 1.5rem;
    border-radius: 4px;
    font-size: 1rem;
    cursor: pointer;
    transition: background-color 0.3s;
}

.cta-button:hover {
    background-color: #1a252f;
}

/* Features Section - Grid */
.features {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 2rem;
    margin-bottom: 3rem;
}

.feature-card {
    background-color: #f9f9f9;
    padding: 1.5rem;
    border-radius: 8px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    transition: transform 0.3s;
}

.feature-card:hover {
    transform: translateY(-5px);
}

.feature-card h2 {
    color: #2c3e50;
    margin-bottom: 0.5rem;
}

/* Gallery Section - Grid */
.gallery {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1rem;
    margin-bottom: 3rem;
}

.gallery-item {
    background-color: #3498db;
    color: white;
    height: 150px;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 8px;
    font-size: 2rem;
    transition: all 0.3s;
}

.gallery-item:hover {
    background-color: #2980b9;
}

/* Footer - Flexbox */
footer {
    background-color: #2c3e50;
    color: white;
    padding: 2rem 0;
}

.footer-content {
    display: flex;
    justify-content: space-between;
    margin-bottom: 1.5rem;
}

.footer-section {
    flex: 1;
    padding: 0 1rem;
}

.footer-section h3 {
    margin-bottom: 1rem;
    font-size: 1.2rem;
}

.footer-section ul {
    list-style: none;
}

.footer-section ul li {
    margin-bottom: 0.5rem;
}

.footer-section a {
    color: #ecf0f1;
    text-decoration: none;
}

.footer-section a:hover {
    text-decoration: underline;
}

.footer-bottom {
    text-align: center;
    padding-top: 1rem;
    border-top: 1px solid #34495e;
}

/* Media Queries */
@media screen and (max-width: 768px) {
    /* Tablet Styles */
    .features {
        grid-template-columns: repeat(2, 1fr);
    }
    
    .gallery {
        grid-template-columns: repeat(2, 1fr);
    }
    
    .footer-content {
        flex-direction: column;
    }
    
    .footer-section {
        margin-bottom: 1.5rem;
    }
}

@media screen and (max-width: 576px) {
    /* Mobile Styles */
    .nav-links {
        position: absolute;
        right: 0;
        top: 70px;
        background-color: #2c3e50;
        flex-direction: column;
        width: 100%;
        align-items: center;
        padding: 1rem 0;
        clip-path: circle(0px at 90% -10%);
        transition: all 0.5s ease-out;
    }
    
    .nav-links.active {
        clip-path: circle(1000px at 90% -10%);
    }
    
    .nav-links li {
        margin: 1rem 0;
    }
    
    .burger {
        display: block;
    }
    
    .features {
        grid-template-columns: 1fr;
    }
    
    .gallery {
        grid-template-columns: 1fr;
    }
    
    .hero h1 {
        font-size: 2rem;
    }
}

/* Animation for mobile menu */
.toggle .line1 {
    transform: rotate(-45deg) translate(-5px, 6px);
}
.toggle .line2 {
    opacity: 0;
}
.toggle .line3 {
    transform: rotate(45deg) translate(-5px, -6px);
}



# JavaScript(script.js)
// Mobile menu toggle
const burger = document.querySelector('.burger');
const navLinks = document.querySelector('.nav-links');

burger.addEventListener('click', () => {
    // Toggle nav
    navLinks.classList.toggle('active');
    
    // Burger animation
    burger.classList.toggle('toggle');
});
