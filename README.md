# Fakebridgeon
<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <title>Guthaben Code Scanner</title>
    <script src="https://cdn.jsdelivr.net/npm/tesseract.js@5/dist/tesseract.min.js"></script>
    <style>
        body { font-family: sans-serif; padding: 20px; text-align: center; }
        #preview { max-width: 300px; display: block; margin: 10px auto; }
        .loading { color: blue; display: none; }
    </style>
</head>
<body>

    <h2>Guthaben-Code scannen</h2>
    
    <input type="file" id="imageInput" accept="image/*">
    <br>
    <img id="preview">
    
    <p class="loading" id="status">Verarbeite Bild...</p>

    <div>
        <label for="giftCardCode">Dein Code:</label>
        <input type="text" id="giftCardCode" placeholder="Code wird erkannt...">
        <button onclick="alert('Code eingelöst!')">Einlösen</button>
    </div>

    <script>
        const imageInput = document.getElementById('imageInput');
        const preview = document.getElementById('preview');
        const codeInput = document.getElementById('giftCardCode');
        const status = document.getElementById('status');

        imageInput.addEventListener('change', (e) => {
            const file = e.target.files[0];
            if (!file) return;

            // Bildvorschau anzeigen
            preview.src = URL.createObjectURL(file);
            status.style.display = 'block';
            codeInput.value = "Lade...";

            // Texterkennung starten
            Tesseract.recognize(
                file,
                'eng', // Sprache (eng funktioniert für Codes meist am besten)
                { logger: m => console.log(m) }
            ).then(({ data: { text } }) => {
                // Den erkannten Text säubern (Leerzeichen/Umbrüche entfernen)
                const cleanCode = text.replace(/\s+/g, '').toUpperCase();
                codeInput.value = cleanCode;
                status.style.display = 'none';
            }).catch(err => {
                console.error(err);
                status.innerText = "Fehler bei der Erkennung.";
            });
        });
    </script>
</body>
</html>
