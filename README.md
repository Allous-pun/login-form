this is a js project
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login and Sign Up</title>
    <style>
        body {
            font-family: Arial, sans-serif;
        }
        .container {
            max-width: 400px;
            margin: 0 auto;
            text-align: center;
        }
        .form {
            background-color: #f2f2f2;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.2);
        }
        input[type="text"], input[type="password"] {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        button {
            width: 100%;
            padding: 10px;
            background-color: #007bff;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="form" id="login-form">
            <h2>Login</h2>
            <input type="text" id="login-username" placeholder="Username">
            <input type="password" id="login-password" placeholder="Password">
            <button onclick="login()">Login</button>
        </div>
        <div class="form" id="signup-form" style="display: none;">
            <h2>Sign Up</h2>
            <input type="text" id="signup-username" placeholder="Username">
            <input type="password" id="signup-password" placeholder="Password">
            <button onclick="signup()">Sign Up</button>
        </div>
        <p>Don't have an account? <a href="javascript:;" onclick="toggleForm()">Sign Up</a></p>
    </div>

    <script>
        function login() {
            const username = document.getElementById('login-username').value;
            const password = document.getElementById('login-password').value;
            // Implement your login logic here
            alert(`Login clicked with Username: ${username} and Password: ${password}`);
        }

        function signup() {
            const username = document.getElementById('signup-username').value;
            const password = document.getElementById('signup-password').value;
            // Implement your sign-up logic here
            alert(`Sign Up clicked with Username: ${username} and Password: ${password}`);
        }

        function toggleForm() {
            const loginForm = document.getElementById('login-form');
            const signupForm = document.getElementById('signup-form');
            if (loginForm.style.display === 'block') {
                loginForm.style.display = 'none';
                signupForm.style.display = 'block';
            } else {
                loginForm.style.display = 'block';
                signupForm.style.display = 'none';
            }
        }
    </script>
</body>
</html>

