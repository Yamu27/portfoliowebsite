

1. HTML 

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>My Portfolio</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>

    <!-- Header Section -->
    <header id="header">
        <div class="container">
            <h1>Welcome to My Portfolio</h1>
            <p>Web Developer | Designer | Programmer</p>
            <a href="#about" class="btn">Learn More</a>
        </div>
    </header>

    <!-- About Section -->
    <section id="about">
        <div class="container">
            <h2>About Me</h2>
            <p>I'm a web developer with a passion for building beautiful and functional websites. I specialize in front-end development and have a deep understanding of JavaScript, CSS, and HTML.</p>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills">
        <div class="container">
            <h2>My Skills</h2>
            <div class="skills-list">
                <div class="skill">
                    <h3>HTML5</h3>
                    <div class="progress-bar"><span style="width: 90%;"></span></div>
                </div>
                <div class="skill">
                    <h3>CSS3</h3>
                    <div class="progress-bar"><span style="width: 80%;"></span></div>
                </div>
                <div class="skill">
                    <h3>JavaScript</h3>
                    <div class="progress-bar"><span style="width: 85%;"></span></div>
                </div>
                <div class="skill">
                    <h3>React</h3>
                    <div class="progress-bar"><span style="width: 70%;"></span></div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <div class="container">
            <h2>Contact Me</h2>
            <form id="contact-form">
                <input type="text" id="name" placeholder="Your Name" required>
                <input type="email" id="email" placeholder="Your Email" required>
                <textarea id="message" placeholder="Your Message" required></textarea>
                <button type="submit" class="btn">Send Message</button>
            </form>
        </div>
    </section>

    <footer>
        <p>&copy; 2024 My Portfolio | All Rights Reserved</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>

2. CSS (styles.css)

/* Global Styles */
body {
    font-family: 'Arial', sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

.container {
    width: 80%;
    margin: auto;
}

/* Header Section */
#header {
    background: #333;
    color: white;
    text-align: center;
    padding: 100px 0;
}

#header h1 {
    font-size: 48px;
    margin: 0;
}

#header p {
    font-size: 24px;
}

.btn {
    background: #007BFF;
    color: white;
    padding: 10px 20px;
    border: none;
    cursor: pointer;
    text-decoration: none;
}

.btn:hover {
    background: #0056b3;
}

/* About Section */
#about {
    padding: 50px 0;
    background-color: #f4f4f4;
    text-align: center;
}

#about h2 {
    margin-bottom: 20px;
}

#about p {
    font-size: 18px;
}

/* Skills Section */
#skills {
    padding: 50px 0;
    text-align: center;
}

#skills h2 {
    margin-bottom: 30px;
}

.skills-list {
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
}

.skill {
    width: 45%;
    margin-bottom: 20px;
}

.skill h3 {
    margin-bottom: 10px;
}

.progress-bar {
    background: #ddd;
    border-radius: 10px;
    overflow: hidden;
    position: relative;
    height: 20px;
}

.progress-bar span {
    background: #007BFF;
    display: block;
    height: 100%;
    border-radius: 10px;
}

/* Contact Section */
#contact {
    padding: 50px 0;
    text-align: center;
    background-color: #f4f4f4;
}

#contact h2 {
    margin-bottom: 20px;
}

#contact-form {
    display: flex;
    flex-direction: column;
    width: 50%;
    margin: auto;
}

#contact-form input, #contact-form textarea {
    margin-bottom: 20px;
    padding: 10px;
    border: 1px solid #ddd;
    border-radius: 5px;
}

#contact-form textarea {
    height: 150px;
}

#contact-form .btn {
    width: 50%;
    margin: auto;
}

footer {
    background: #333;
    color: white;
    text-align: center;
    padding: 10px 0;
}

3. JavaScript (script.js)

document.getElementById('contact-form').addEventListener('submit', function(event) {
    event.preventDefault(); // Prevent the form from submitting
    const name = document.getElementById('name').value;
    const email = document.getElementById('email').value;
    const message = document.getElementById('message').value;

    // Simple form validation
    if (name && email && message) {
        alert("Thank you for your message!");
    } else {
        alert("Please fill out all fields.");
    }
});

