<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cambridge Login - Aktiv</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #4db6ac; /* Original Türkis */
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        .login-card {
            background: white;
            width: 90%;
            max-width: 400px;
            padding: 30px;
            text-align: center;
            box-shadow: 0 10px 25px rgba(0,0,0,0.2);
            border-radius: 8px;
        }

        h2 { color: #333; margin-bottom: 20px; font-weight: 500; }

        /* Input Styles */
        .input-group {
            text-align: left;
            margin-bottom: 20px;
        }

        label { 
            display: block; 
            margin-bottom: 8px; 
            font-weight: 600; 
            font-size: 0.85em; 
            color: #444;
        }

        input {
            width: 100%;
            padding: 14px;
            border: 1px solid #ddd;
            background-color: #fcfcfc;
            border-radius: 4px;
            box-sizing: border-box;
            transition: border 0.3s;
        }

        input:focus {
            outline: none;
            border-color: #7c4dff;
            background-color: #fff;
        }

        /* Der lila Login-Button */
        .btn-login {
            background-color: #7c4dff;
            color: white;
            border: none;
            padding: 14px;
            width: 100%;
            border-radius: 30px;
            font-size: 1em;
            font-weight: bold;
            cursor: pointer;
            transition: background 0.3s, transform 0.1s;
        }

        .btn-login:hover {
            background-color: #6a3de8;
        }

        .btn-login:active {
            transform: scale(0.98);
        }

        .footer-links {
            margin-top: 20px;
            font-size: 0.9em;
        }

        .footer-links a {
            color: #7c4dff;
            text-decoration: none;
            font-weight: bold;
        }
    </style>
</head>
<body>

    <div class="login-card">
        <h2>Log in</h2>

        <form id="loginForm">
            <div class="input-group">
                <label for="username">Login</label>
                <input type="text" id="username" name="username" placeholder="E-Mail oder Benutzername" required>
            </div>

            <div class="input-group">
                <label for="password">Password</label>
                <input type="password" id="password" name="password" placeholder="Passwort eingeben" required>
            </div>

            <button type="submit" class="btn-login">Log in</button>
        </form>

        <div class="footer-links">
            <p><a href="#">Passwort vergessen?</a></p>
            <p>Noch kein Konto? <a href="#">Hier registrieren</a></p>
        </div>
    </div>

    <script>
        // Funktion, die beim Abschicken ausgeführt wird
        document.getElementById('loginForm').addEventListener('submit', function(event) {
            event.preventDefault(); // Verhindert das Neuladen der Seite

            const user = document.getElementById('username').value;
            const pass = document.getElementById('password').value;

            // Hier würde normalerweise die Prüfung gegen eine Datenbank stehen
            alert("Versuchter Login!\nBenutzer: " + user + "\nPasswort: " + pass);
            
            console.log("Daten gesendet:", { user, pass });
        });
    </script>

</body>
</html>
