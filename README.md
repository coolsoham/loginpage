# loginpage
#this a basic html css and javascript file which gives a basic idea of how to create a webpage

HTML file

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login Page</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="login-container">
        <div class="form-container">
            <h2>Welcome Back</h2>
            <form id="loginForm">
                <div class="input-group">
                    <label for="email">Email</label>
                    <input type="email" id="email" name="email" required>
                </div>
                <div class="input-group">
                    <label for="password">Password</label>
                    <input type="password" id="password" name="password" required>
                </div>
                <button type="submit" class="btn">Login</button>
            </form>
            <p class="footer-text">Don't have an account? <a href="#">Sign up</a></p>
        </div>
    </div>
    <script src="script.js"></script>
</body>
</html>

CSS File
/* General Styles */
* {
    margin: 1;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Arial', sans-serif;
}

/* Body Styles */
body {
    background: linear-gradient(135deg, #74ebd5, #9face6);
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    color: #333;
}

/* Login Container */
.login-container {
    background: white;
    padding: 2rem;
    border-radius: 10px;
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
    max-width: 400px;
    width: 100%;
}

/* Form Container */
.form-container h2 {
    text-align: center;
    margin-bottom: 1.5rem;
    color: #5d5c61;
}

/* Input Group */
.input-group {
    margin-bottom: 1.2rem;
}

.input-group label {
    display: block;
    margin-bottom: 0.5rem;
    font-size: 0.9rem;
    color: #5d5c61;
}

.input-group input {
    width: 100%;
    padding: 0.8rem;
    border: 1px solid #ccc;
    border-radius: 5px;
    font-size: 1rem;
}

/* Button */
.btn {
    width: 100%;
    padding: 0.8rem;
    background: #74ebd5;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 1rem;
    transition: background 0.3s;
}

.btn:hover {
    background: #5ab9d0;
}

/* Footer Text */
.footer-text {
    text-align: center;
    margin-top: 1rem;
    font-size: 0.9rem;
}

.footer-text a {
    color: #74ebd5;
    text-decoration: none;
    font-weight: bold;
}

.footer-text a:hover {
    text-decoration: underline;
}

JAVASCRIPT file
document.getElementById('loginForm').addEventListener('submit', function (e) {
    e.preventDefault();

    const email = document.getElementById('email').value;
    const password = document.getElementById('password').value;

    if (email && password) {
        alert(`Welcome, ${email}! You have successfully logged in.`);
    } else {
        alert('Please fill in all fields.');
    }
});
