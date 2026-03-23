<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cambridge Login Demo</title>
    <style>
        /* Grunddesign */
        body {
            margin: 0;
            padding: 0;
            font-family: Arial, sans-serif;
            background-color: #4db6ac; /* Die türkise Hintergrundfarbe aus deinem Bild */
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        /* Die weiße Box in der Mitte */
        .login-card {
            background: white;
            width: 100%;
            max-width: 400px;
            padding: 40px;
            text-align: center;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
            border-radius: 4px;
        }

        h2 { color: #333; margin-bottom: 5px; }
        p.subtitle { color: #777; font-size: 0.9em; margin-bottom: 20px; }

        /* Social Buttons */
        .social-buttons {
            display: flex;
            flex-direction: column;
            gap: 10px;
            margin-bottom: 20px;
        }

        .btn-social {
            padding: 10px;
            border: 1px solid #ddd;
            background: #fff;
            color: #555;
            cursor: not-allowed; /* Zeigt, dass man nichts machen kann */
            opacity: 0.6;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
        }

        /* Eingabefelder */
        .input-group {
            text-align: left;
            margin-bottom: 15px;
        }

        label { display: block; margin-bottom: 5px; font-weight: bold; font-size: 0.9em; }

        input {
            width: 100%;
            padding: 12px;
            border: 1px solid #eee;
            background-color: #f9f9f9;
            box-sizing: border-box;
            cursor: not-allowed;
        }

        /* Der lila Button */
        .btn-login {
            background-color: #7c4dff;
            color: white;
            border: none;
            padding: 15px;
            width: 100%;
            border-radius: 25px;
            font-size: 1em;
            font-weight: bold;
            cursor: not-allowed;
            opacity: 0.7;
            margin-top: 10px;
        }

        .links {
            margin-top: 15px;
            font-size: 0.85em;
            color: #7c4dff;
            text-decoration: underline;
        }
    </style>
</head>
<body>

    <div class="login-card">
        <h2>Log in</h2>
        <p class="subtitle">with</p>

        <div class="social-buttons">
            <button class="btn-social" disabled>Facebook</button>
            <button class="btn-social" disabled>Google</button>
            <button class="btn-social" disabled>Apple</button>
        </div>

        <p class="subtitle">or</p>

        <div class="input-group">
            <label>Login</label>
            <input type="text" placeholder="Enter your username or email address" disabled>
        </div>

        <div class="input-group">
            <label>Password</label>
            <input type="password" placeholder="Enter your password" disabled>
        </div>

        <button class="btn-login" disabled>Log in</button>

        <div class="links">
            Don't have an account yet?
        </div>
    </div>

</body>
</html> 
