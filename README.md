# Ex02 Commercial Website
## Date:30/10/2026

## AIM
To create a commercial website using CSS Flexbox.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for Homepage, Products / Services, About Us, Contact Details and User Account.

### STEP 5
Include social media links at the footer with copyright information.

### STEP 6
Define global styles for fonts, colors, and layout.

### STEP 7
Style the header, navigation bar, and sections.

### STEP 8
Use Flexbox for layout design.

### STEP 9
Add hover effects and transitions for interactivity.

### STEP 10
Add Images and Media.

### STEP 11
Use optimized images for a professional look.

### STEP 12
Open the HTML file in a browser to check layout and functionality.

### STEP 13
Fix styling issues and refine content placement.

### STEP 14
Deploy the website.

### STEP 15
Upload to GitHub Pages for free hosting.

## PROGRAM

index.html

```
<!DOCTYPE html>
<html>
<head>
    <title>Bluebell Boutique | Home</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: Arial, sans-serif;
            background-color: #F5EBDD;
            color: #263445;
        }

        /* Header */
        header {
            background-color: #142D4E;
            color: #FFF9F1;
            padding: 22px 7%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 15px;
        }

        .logo h1 {
            font-family: Georgia, serif;
            letter-spacing: 2px;
            font-size: 28px;
        }

        .logo p {
            color: #D8C3A5;
            font-size: 13px;
            margin-top: 5px;
        }

        /* Navigation */
        nav {
            display: flex;
            justify-content: center;
            align-items: center;
            flex-wrap: wrap;
            gap: 25px;
            background-color: #0B1F35;
            padding: 15px;
        }

        nav a {
            color: #FFF9F1;
            text-decoration: none;
            font-weight: bold;
            font-size: 14px;
        }

        nav a:hover {
            color: #D8C3A5;
        }

        /* Search Bar */
        .search-container {
            display: flex;
            justify-content: center;
            padding: 18px;
            background-color: #F5EBDD;
        }

        .search-container form {
            display: flex;
            width: 90%;
            max-width: 520px;
        }

        .search-container input {
            flex: 1;
            min-width: 0;
            padding: 12px 15px;
            border: 1px solid #C7B69D;
            border-radius: 25px 0 0 25px;
            font-size: 14px;
        }

        .search-container button {
            background-color: #142D4E;
            color: white;
            border: none;
            padding: 12px 22px;
            border-radius: 0 25px 25px 0;
            cursor: pointer;
        }

        /* Hero Section */
        .hero {
            background-color: #E6D7C3;
            display: flex;
            justify-content: space-around;
            align-items: center;
            flex-wrap: wrap;
            gap: 25px;
            padding: 45px 7%;
        }

        .hero-text {
            flex: 1;
            min-width: 250px;
        }

        .hero-text h2 {
            font-family: Georgia, serif;
            font-size: 38px;
            color: #142D4E;
            margin-bottom: 15px;
        }

        .hero-text p {
            font-size: 16px;
            line-height: 1.7;
            margin-bottom: 22px;
        }

        .hero-text a {
            display: inline-block;
            background-color: #142D4E;
            color: #FFF9F1;
            text-decoration: none;
            padding: 13px 25px;
            border-radius: 25px;
            font-weight: bold;
        }

        .hero-text a:hover {
            background-color: #0B1F35;
        }

        .hero-image {
            flex: 1;
            min-width: 250px;
            text-align: center;
        }

        .hero-image img {
            width: 100%;
            max-width: 420px;
            height: 300px;
            object-fit: cover;
            border-radius: 15px;
        }

        /* Section Headings */
        .section-heading {
            text-align: center;
            padding: 35px 15px 10px;
        }

        .section-heading h2 {
            font-family: Georgia, serif;
            color: #142D4E;
            font-size: 28px;
            margin-bottom: 8px;
        }

        .section-heading p {
            color: #6B6258;
        }

        /* Categories */
        .categories {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 20px;
            padding: 25px 7% 40px;
        }

        .category-card {
            background-color: #FFF9F1;
            width: 200px;
            padding: 12px;
            border-radius: 12px;
            text-align: center;
            box-shadow: 0 4px 12px #142D4E15;
        }

        .category-card img {
            width: 100%;
            height: 145px;
            object-fit: cover;
            border-radius: 8px;
        }

        .category-card h3 {
            color: #142D4E;
            margin-top: 12px;
        }

        /* Featured Products */
        .products {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 22px;
            padding: 25px 7% 45px;
        }

        .product-card {
            background-color: #FFF9F1;
            width: 230px;
            padding: 15px;
            border-radius: 12px;
            text-align: center;
            display: flex;
            flex-direction: column;
            align-items: center;
            box-shadow: 0 4px 14px #142D4E18;
        }

        .product-card img {
            width: 100%;
            height: 175px;
            object-fit: cover;
            border-radius: 8px;
            margin-bottom: 13px;
        }

        .product-card h3 {
            color: #142D4E;
            margin-bottom: 8px;
        }

        .product-card p {
            margin-bottom: 14px;
            color: #6B6258;
        }

        .product-card button {
            background-color: #142D4E;
            color: #FFF9F1;
            border: none;
            padding: 10px 20px;
            border-radius: 22px;
            cursor: pointer;
            margin-top: auto;
        }

        .product-card button:hover {
            background-color: #0B1F35;
        }

        /* Promotion Banner */
        .promotion {
            background-color: #142D4E;
            color: #FFF9F1;
            text-align: center;
            padding: 35px 15px;
        }

        .promotion h2 {
            font-family: Georgia, serif;
            font-size: 28px;
            margin-bottom: 10px;
        }

        .promotion p {
            color: #E6D7C3;
            margin-bottom: 18px;
        }

        .promotion a {
            display: inline-block;
            background-color: #E6D7C3;
            color: #142D4E;
            text-decoration: none;
            padding: 11px 22px;
            border-radius: 25px;
            font-weight: bold;
        }

        /* Footer */
        footer {
            background-color: #0B1F35;
            color: #F5EBDD;
            padding: 25px 15px;
            text-align: center;
            line-height: 1.8;
        }

        footer a {
            color: #D8C3A5;
            text-decoration: none;
        }

        /* Responsive Design */
        @media (max-width: 650px) {
            header {
                justify-content: center;
                text-align: center;
            }

            nav {
                flex-direction: column;
                gap: 14px;
            }

            .hero {
                flex-direction: column;
                text-align: center;
            }

            .hero-text h2 {
                font-size: 30px;
            }

            .hero-image img {
                height: 230px;
            }

            .categories,
            .products {
                flex-direction: column;
                align-items: center;
            }

            .category-card,
            .product-card {
                width: 90%;
                max-width: 320px;
            }
        }
    </style>
</head>

<body>

    <!-- Header -->
    <header id="home">
        <div class="logo">
            <h1>BLUEBELL BOUTIQUE</h1>
            <p>Timeless pieces. Everyday elegance.</p>
        </div>
    </header>

    <!-- Navigation -->
    <nav>
        <a href="index.html">Home</a>
        <a href="products.html">Products</a>
        <a href="offers.html">Offers</a>
        <a href="contact.html">Contact</a>
    </nav>

    <!-- Search Bar -->
    <div class="search-container">
        <form action="products.html" method="get">
            <input type="search"
                   name="search"
                   placeholder="Search for your favorite products..."
                   aria-label="Search products">
            <button type="submit">Search</button>
        </form>
    </div>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-text">
            <h2>Discover Your Everyday Style</h2>
            <p>
                Explore thoughtfully selected fashion accessories
                that bring elegance and comfort to your everyday look.
            </p>
            <a href="products.html">Shop Collection</a>
        </div>

        <div class="hero-image">
            <img src="https://images.unsplash.com/photo-1483985988355-763728e1935b?auto=format&fit=crop&w=900&q=80"
                 alt="Fashion collection">
        </div>
    </section>

    <!-- Categories -->
    <section>
        <div class="section-heading">
            <h2>Shop by Category</h2>
            <p>Find the perfect pieces for your style.</p>
        </div>

        <div class="categories">
            <div class="category-card">
                <img src="https://images.unsplash.com/photo-1584917865442-de89df76afd3?auto=format&fit=crop&w=600&q=80"
                     alt="Handbags">
                <h3>Handbags</h3>
            </div>

            <div class="category-card">
                <img src="https://images.unsplash.com/photo-1543163521-1bf539c55dd2?auto=format&fit=crop&w=600&q=80"
                     alt="Shoes">
                <h3>Footwear</h3>
            </div>

            <div class="category-card">
                <img src="https://images.unsplash.com/photo-1523275335684-37898b6baf30?auto=format&fit=crop&w=600&q=80"
                     alt="Watches">
                <h3>Watches</h3>
            </div>

            <div class="category-card">
                <img src="https://images.unsplash.com/photo-1511499767150-a48a237f0083?auto=format&fit=crop&w=600&q=80"
                     alt="Sunglasses">
                <h3>Sunglasses</h3>
            </div>
        </div>
    </section>

    <!-- Featured Products -->
    <section id="featured">
        <div class="section-heading">
            <h2>Featured Products</h2>
            <p>Our stylish picks for you.</p>
        </div>

        <div class="products">
            <div class="product-card">
                <img src="https://images.unsplash.com/photo-1584917865442-de89df76afd3?auto=format&fit=crop&w=600&q=80"
                     alt="Classic Handbag">
                <h3>Classic Handbag</h3>
                <p>₹999</p>
                <button type="button">Shop Now</button>
            </div>

            <div class="product-card">
                <img src="https://images.unsplash.com/photo-1543163521-1bf539c55dd2?auto=format&fit=crop&w=600&q=80"
                     alt="Casual Shoes">
                <h3>Casual Shoes</h3>
                <p>₹1,499</p>
                <button type="button">Shop Now</button>
            </div>

            <div class="product-card">
                <img src="https://images.unsplash.com/photo-1523275335684-37898b6baf30?auto=format&fit=crop&w=600&q=80"
                     alt="Elegant Watch">
                <h3>Elegant Watch</h3>
                <p>₹1,299</p>
                <button type="button">Shop Now</button>
            </div>

            <div class="product-card">
                <img src="https://images.unsplash.com/photo-1511499767150-a48a237f0083?auto=format&fit=crop&w=600&q=80"
                     alt="Fashion Sunglasses">
                <h3>Fashion Sunglasses</h3>
                <p>₹599</p>
                <button type="button">Shop Now</button>
            </div>
        </div>
    </section>

    <!-- Promotional Banner -->
    <section class="promotion" id="offers">
        <h2>A Little Something Special</h2>
        <p>Enjoy up to 20% off on selected boutique favorites.</p>
        <a href="offers.html">Explore Offers</a>
    </section>

    <!-- Footer -->
    <footer id="contact">
        <p><b>BLUEBELL BOUTIQUE</b></p>
        <p>Timeless pieces. Everyday elegance.</p>
        <p>
            <a href="products.html">Products</a> |
            <a href="offers.html">Offers</a> |
            <a href="contact.html">Contact</a>
        </p>
        <p>Contact: bluebellboutique@example.com</p>
        <p>© 2026 Bluebell Boutique. All rights reserved.</p>
    </footer>

</body>
</html>



```


style.css

```
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    font-family: Arial, sans-serif;
    background-color: #F5EBDD;
    color: #2D2D2D;
}

header {
    background-color: #142D4E;
    color: #FFF9F1;
    text-align: center;
    padding: 25px;
}

header h1 {
    margin-bottom: 8px;
    letter-spacing: 2px;
}

nav {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 25px;
    background-color: #0B1F35;
    padding: 15px;
}

nav a {
    color: #F5EBDD;
    text-decoration: none;
    font-weight: bold;
}

nav a:hover {
    color: #D8C3A5;
}

.banner {
    background-color: #FFF9F1;
    text-align: center;
    padding: 35px 15px;
}

.banner h2 {
    color: #142D4E;
    margin-bottom: 10px;
}

.products {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 25px;
    padding: 30px;
}

.product-card {
    background-color: #FFF9F1;
    border: 1px solid #D8C3A5;
    border-radius: 10px;
    width: 220px;
    padding: 15px;
    text-align: center;

    display: flex;
    flex-direction: column;
    align-items: center;
}

.product-card img {
    width: 100%;
    height: 160px;
    object-fit: cover;
    border-radius: 8px;
    margin-bottom: 12px;
}

.product-card h3 {
    color: #142D4E;
    margin-bottom: 8px;
}

.product-card p {
    margin-bottom: 15px;
}

.product-card button {
    background-color: #142D4E;
    color: #F5EBDD;
    border: none;
    padding: 10px 15px;
    border-radius: 5px;
    cursor: pointer;
    margin-top: auto;
}

.product-card button:hover {
    background-color: #0B1F35;
}

.content {
    max-width: 900px;
    margin: 30px auto;
    padding: 25px;
    background-color: #FFF9F1;
    border: 1px solid #D8C3A5;
    border-radius: 10px;
}

.content h2 {
    color: #142D4E;
    margin-bottom: 15px;
}

.content p {
    line-height: 1.6;
    margin-bottom: 12px;
}

.offer-box {
    background-color: #D8C3A5;
    padding: 20px;
    margin: 15px 0;
    border-radius: 8px;
}

.offer-box h3 {
    color: #142D4E;
    margin-bottom: 8px;
}

.contact-info {
    text-align: center;
}

.contact-info a {
    color: #142D4E;
    font-weight: bold;
}

footer {
    background-color: #0B1F35;
    color: #F5EBDD;
    text-align: center;
    padding: 20px;
    margin-top: 20px;
}

@media (max-width: 600px) {
    nav {
        flex-direction: column;
        align-items: center;
        gap: 15px;
    }

    .products {
        flex-direction: column;
        align-items: center;
    }

    .product-card {
        width: 90%;
        max-width: 300px;
    }

    .content {
        margin: 20px;
    }
}

/* Search Bar */
.search-container {
    display: flex;
    justify-content: center;
    padding: 20px;
    background-color: #F5EBDD;
}

.search-container form {
    display: flex;
    width: 90%;
    max-width: 500px;
}

.search-container input {
    flex: 1;
    padding: 12px;
    border: 2px solid #142D4E;
    border-radius: 6px 0 0 6px;
    font-size: 15px;
    outline: none;
}

.search-container button {
    background-color: #142D4E;
    color: #F5EBDD;
    border: none;
    padding: 12px 20px;
    border-radius: 0 6px 6px 0;
    cursor: pointer;
}

.search-container button:hover {
    background-color: #0B1F35;
}

@media (max-width: 600px) {
    .search-container form {
        width: 100%;
    }
}




```



## OUTPUT

<img width="1897" height="925" alt="image" src="https://github.com/user-attachments/assets/c39eb64d-1cd4-41df-a2ae-4cdf7ba75bdd" />




## RESULT
The program for creating commercial website using CSS Flexbox is executed successfully.
