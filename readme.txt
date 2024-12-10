index.html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>College Website</title>
    <link rel="stylesheet" href="style.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">
</head>

<body>
    <header>
        <div class="logo">
            <a href="/">My College</a>
        </div>
        <nav>
            <ul id="navbar">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About Us</a></li>
                <li><a href="#courses">Courses</a></li>
                <li><a href="#events">Events</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
            <a href="javascript:void(0);" class="icon" onclick="toggleMenu()">
                <i class="fa fa-bars"></i>
            </a>
        </nav>
    </header>

    <section id="home">
        <div class="home-content">
            <h1>Welcome to kishkinda university</h1>
            <p>Your journey to excellence starts here.</p>
        </div>
    </section>

    <section id="about">
        <div class="about-content">
            <h2>About Us</h2>
            <p>Our college is dedicated to providing the best education in various fields. We offer a range of programs
                designed to prepare students for success in their careers and in life.</p>
                <img src="ku1.jpg">
        </div>
    </section>

    <section id="courses">
        <div class="courses-content">
            <h2>Our Courses</h2>
            <div class="course-list">
                <div class="course-item">
                    <h3>Computer Science</h3>
                    <p>Prepare for a career in the tech industry with our cutting-edge computer science program.</p>
                    <img src ="cs.jpg" height="300 px" width="250 px">
                </div>
                <div class="course-item">
                    <h3>Business Administration</h3>
                    <p>Learn the essential skills for success in business with our Business Administration degree.</p>
                    <img src ="bus.jpg" height="300 px" width="250 px">
                </div>
                <div class="course-item">
                    <h3>Engineering</h3>
                    <p>Our engineering programs provide students with the knowledge and skills to solve real-world problems.</p>
                    <img src ="eng.jpg" height="300 px" width="250 px">
                </div>
            </div>
        </div>
    </section>

    <section id="events">
        <div class="events-content">
            <h2>Upcoming Events</h2>
            <ul><h3>
                <li><strong>feb 20, 2025:</strong>explorika 2k25 </li>
                <li><strong>aug 22, 2025:</strong> college fest</li>
                <li><strong>dec 15, 2025:</strong> freshers day</li></h3>
            </ul>
        </div>
    </section>

    <section id="contact">
        <div class="contact-content">
            <h2>Contact Us</h2>
            <form id="contactForm">
                <label for="name">Name</label>
                <input type="text" id="name" name="name" required>
                
                <label for="email">Email</label>
                <input type="email" id="email" name="email" required>
                
                <label for="message">Message</label>
                <textarea id="message" name="message" required></textarea>
                
                <button type="submit">Send Message</button>
            </form>
        </div>
    </section>

    <footer>
        <p>&copy; 2024 My College. All rights reserved.</p>
    </footer>

    <script src="script.js"></script>
</body>

</html>


style.css

/* Global styles */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

header {
    background-color: #333;
    padding: 10px 0;
    color: white;
    text-align: center;
}

header .logo a {
    font-size: 2rem;
    text-decoration: none;
    color: white;
}

nav ul {
    list-style-type: none;
    padding: 0;
    margin: 0;
    display: flex;
    justify-content: center;
}

nav ul li {
    margin: 0 15px;
}

nav ul li a {
    text-decoration: none;
    color: white;
    font-size: 1.2rem;
}

nav .icon {
    display: none;
}

section {
    padding: 50px 20px;
    text-align: center;
}

section#home {
    background-color: #4CAF50;
    color: white;
}

section#about, section#courses, section#events, section#contact {
    background-color: #f4f4f4;
}

section#courses .course-list {
    display: flex;
    justify-content: space-around;
    margin-top: 30px;
}

section#courses .course-item {
    background-color: #fff;
    padding: 20px;
    border: 1px solid #ddd;
    width: 30%;
}

form {
    display: flex;
    flex-direction: column;
    max-width: 600px;
    margin: 0 auto;
}

form input, form textarea {
    margin: 10px 0;
    padding: 10px;
    font-size: 1rem;
    border: 1px solid #ddd;
}

form button {
    padding: 10px 20px;
    background-color: #333;
    color: white;
    border: none;
    cursor: pointer;
}

footer {
    text-align: center;
    padding: 10px;
    background-color: #333;
    color: white;
}

@media (max-width: 768px) {
    nav ul {
        display: none;
        flex-direction: column;
        align-items: center;
    }

    nav ul li {
        margin: 10px 0;
    }

    nav ul.responsive {
        display: flex;
    }

    nav .icon {
        display: block;
        cursor: pointer;
    }

    section#courses .course-list {
        flex-direction: column;
    }

    section#courses .course-item {
        width: 80%;
        margin: 10px auto;
    }
}

script.js

function toggleMenu() {
    var navbar = document.getElementById("navbar");
    if (navbar.className === "") {
        navbar.className = "responsive";
    } else {
        navbar.className = "KISHKINDA UNIVERSITY";
    }
}

