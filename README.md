<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NQsha | Premium Car Upholstery</title>
    <style>
        /* --- RESET & BASIC STYLES --- */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f4f4f4;
            color: #333;
            line-height: 1.6;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        ul {
            list-style: none;
        }

        /* --- COLORS --- */
        :root {
            --primary: #111111; /* Dark Black */
            --accent: #d35400; /* Burnt Orange */
            --light: #ffffff;
            --gray: #f4f4f4;
        }

        /* --- NAVIGATION --- */
        .navbar {
            background-color: var(--primary);
            color: var(--light);
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 2rem;
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            letter-spacing: 2px;
            color: var(--accent);
        }

        .nav-links {
            display: flex;
            gap: 20px;
        }

        .nav-links a {
            color: var(--light);
            transition: color 0.3s;
            font-weight: 500;
        }

        .nav-links a:hover {
            color: var(--accent);
        }

        .cta-btn {
            background-color: var(--accent);
            color: var(--light);
            padding: 0.5rem 1.2rem;
            border-radius: 4px;
            font-weight: bold;
        }

        .cta-btn:hover {
            background-color: #e67e22;
        }

        /* --- HERO SECTION --- */
        .hero {
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('https://images.unsplash.com/photo-1552519507-da3b142c6e3d?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            height: 80vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: var(--light);
            padding: 0 20px;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            text-transform: uppercase;
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            max-width: 600px;
        }

        .hero-btn {
            background-color: var(--accent);
            color: var(--light);
            padding: 1rem 2rem;
            font-size: 1.1rem;
            border-radius: 5px;
            border: none;
            cursor: pointer;
            transition: background 0.3s;
        }

        .hero-btn:hover {
            background-color: #e67e22;
        }

        /* --- SERVICES SECTION --- */
        .section {
            padding: 4rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: var(--primary);
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .service-card {
            background: var(--light);
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            text-align: center;
            transition: transform 0.3s;
        }

        .service-card:hover {
            transform: translateY(-5px);
        }

        .service-icon {
            font-size: 3rem;
            color: var(--accent);
            margin-bottom: 1rem;
        }

        .service-card h3 {
            margin-bottom: 1rem;
            font-size: 1.5rem;
        }

        /* --- GALLERY / PORTFOLIO --- */
        .gallery {
            background-color: var(--primary);
            color: var(--light);
        }

        .gallery .section-title {
            color: var(--light);
        }

        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1rem;
        }

        .gallery-item {
            height: 250px;
            background-color: #333;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 4px;
            overflow: hidden;
        }
        
        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.3s;
        }

        .gallery-item:hover img {
            transform: scale(1.1);
        }

        /* --- CONTACT SECTION --- */
        .contact-container {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            justify-content: center;
        }

        .contact-info, .contact-form {
            flex: 1;
            min-width: 300px;
            background: var(--light);
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }

        .contact-info h3 {
            margin-bottom: 1rem;
            color: var(--accent);
        }

        .contact-info p {
            margin-bottom: 0.5rem;
        }

        form input, form textarea {
            width: 100%;
            padding: 0.8rem;
            margin-bottom: 1rem;
            border: 1px solid #ccc;
            border-radius: 4px;
        }

        form button {
            width: 100%;
            background-color: var(--primary);
            color: var(--light);
            padding: 1rem;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 1rem;
        }

        form button:hover {
            background-color: var(--accent);
        }

        /* --- FOOTER --- */
        footer {
            background-color: #000;
            color: #888;
            text-align: center;
            padding: 2rem;
            margin-top: 2rem;
        }

        /* --- MOBILE RESPONSIVENESS --- */
        @media (max-width: 768px) {
            .hero h1 { font-size: 2.5rem; }
            .nav-links { display: none; } /* Ideally add a hamburger menu here */
            .navbar { flex-direction: column; gap: 1rem; }
        }
    </style>
</head>
<body>

    <!-- Header -->
    <nav class="navbar">
        <div class="logo">NQSHA</div>
        <ul class="nav-links">
            <li><a href="#home">Home</a></li>
            <li><a href="#services">Services</a></li>
            <li><a href="#gallery">Gallery</a></li>
            <li><a href="#contact" class="cta-btn">Get a Quote</a></li>
        </ul>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <h1>Restore. Redesign. Revitalize.</h1>
        <p>The premier destination for luxury car interiors, custom upholstery, and leather restoration.</p>
        <button class="hero-btn" onclick="document.getElementById('contact').scrollIntoView()">Start Your Project</button>
    </section>

    <!-- Services Section -->
    <section id="services" class="section">
        <h2 class="section-title">Our Expertise</h2>
        <div class="services-grid">
            <div class="service-card">
                <div class="service-icon">🧵</div>
                <h3>Leather Repair</h3>
                <p>We fix rips, tears, scratches, and restore faded colors to make your interior look factory new.</p>
            </div>
            <div class="service-card">
                <div class="service-icon">🛋️</div>
                <h3>Full Upholstery</h3>
                <p>Complete reupholstery services using premium Leather, Alcantara, or Fabric materials.</p>
            </div>
            <div class="service-card">
                <div class="service-icon">✨</div>
                <h3>Custom Stitching</h3>
                <p>Add a personal touch with custom diamond stitching, embroidery, and unique patterns.</p>
            </div>
        </div>
    </section>

    <!-- Gallery Section -->
    <section id="gallery" class="section gallery">
        <h2 class="section-title">Recent Work</h2>
        <div class="gallery-grid">
            <!-- Placeholder images from Unsplash -->
            <div class="gallery-item">
                <img src="https://images.unsplash.com/photo-1601362840469-51e4d8d58785?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="Car Interior">
            </div>
            <div class="gallery-item">
                <img src="https://images.unsplash.com/photo-1492144534655-ae79c964c9d7?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="Leather Seats">
            </div>
            <div class="gallery-item">
                <img src="https://images.unsplash.com/photo-1494905998402-395d579af97f?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="Car Detail">
            </div>
            <div class="gallery-item">
                <img src="https://images.unsplash.com/photo-1552519507-da3b142c6e3d?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="Upholstery Work">
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="section">
        <h2 class="section-title">Contact NQsha</h2>
        <div class="contact-container">
            <div class="contact-info">
                <h3>Visit the Shop</h3>
                <p><strong>Address:</strong> 123 Auto Lane, Car City, ST 12345</p>
                <p><strong>Phone:</strong> (555) 123-4567</p>
                <p><strong>Email:</strong> hello@nqsha.com</p>
                <br>
                <h3>Hours</h3>
                <p>Mon - Fri: 8:00 AM - 6:00 PM</p>
                <p>Saturday: 9:00 AM - 2:00 PM</p>
                <p>Sunday: Closed</p>
            </div>
            <div class="contact-form">
                <h3>Request a Quote</h3>
                <form>
                    <input type="text" placeholder="Your Name" required>
                    <input type="email" placeholder="Your Email" required>
                    <input type="text" placeholder="Car Make & Model" required>
                    <textarea rows="5" placeholder="Describe the service you need..." required></textarea>
                    <button type="submit">Send Message</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2023 NQsha Upholstery. All Rights Reserved.</p>
    </footer>

</body>
</html>
