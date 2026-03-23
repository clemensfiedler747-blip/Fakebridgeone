<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Cambridge One</title>

    <!-- Standard favicon (.ico) -->
    <link rel="icon" href="assets/icon.ico" type="image/x-icon">

    <!-- PNG favicon for modern browsers -->
    <link rel="icon" href="assets/icon.png" type="image/png">

    <!-- Apple Touch Icon (iOS Home Screen) -->
    <link rel="apple-touch-icon" href="assets/icon.png">

    <!-- iOS Web App Meta Tags -->
    <meta name="apple-mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
    <meta name="apple-mobile-web-app-title" content="Cambridge One">

    <style>
        body, html {
            margin: 0;
            padding: 0;
            width: 100%;
            height: 100%;
            overflow: hidden;
            background-color: #000;
        }

        .fullscreen-container {
            width: 100vw;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .fullscreen-image {
            width: 100%;
            height: 100%;
            object-fit: fill;
            display: block;
        }

        #error-msg {
            display: none;
            color: white;
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            text-align: center;
            padding: 20px;
        }
    </style>
</head>
<body>

    <div class="fullscreen-container">
        <img 
            src="assets/image.jpeg" 
            alt="Cambridge One" 
            class="fullscreen-image"
            onerror="handleImageError()"
        >
    </div>

    <script>
        function handleImageError() {
            document.querySelector('.fullscreen-image').style.display = 'none';
            document.getElementById('error-msg').style.display = 'block';
        }

        document.addEventListener('touchmove', function(e) {
            e.preventDefault();
        }, { passive: false });
    </script>
</body>
</html>
