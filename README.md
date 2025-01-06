<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Flexibele Arbeidsvoorwaarden</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f9f9f9;
        }
        header {
            background-color: #0073e6;
            color: white;
            padding: 1rem;
            text-align: center;
        }
        .container {
            max-width: 1200px;
            margin: 2rem auto;
            padding: 1rem;
            background: white;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            border-radius: 8px;
        }
        nav {
            display: flex;
            justify-content: center;
            background-color: #005bb5;
            padding: 1rem;
        }
        nav a {
            color: white;
            text-decoration: none;
            margin: 0 1rem;
            font-size: 1.2rem;
        }
        nav a:hover {
            text-decoration: underline;
        }
        .section {
            margin-bottom: 2rem;
        }
        .section h2 {
            margin-top: 0;
            color: #0073e6;
        }
        .option {
            border: 1px solid #ddd;
            border-radius: 5px;
            padding: 1rem;
            margin-bottom: 1rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .option button {
            background-color: #0073e6;
            color: white;
            border: none;
            padding: 0.5rem 1rem;
            border-radius: 5px;
            cursor: pointer;
        }
        .option button:hover {
            background-color: #005bb5;
        }
        footer {
            text-align: center;
            padding: 1rem;
            background-color: #f1f1f1;
            margin-top: 2rem;
            font-size: 0.9rem;
        }
        .choice-container {
            display: flex;
            flex-direction: column;
            align-items: center;
            margin: 2rem 0;
        }
        .choice-container button {
            margin: 1rem;
            padding: 1rem 2rem;
            background-color: #0073e6;
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 1rem;
            cursor: pointer;
        }
        .choice-container button:hover {
            background-color: #005bb5;
        }
        .hidden {
            display: none;
        }
    </style>
</head>
<body>
    <header>
        <h1>Flexibele Arbeidsvoorwaarden</h1>
    </header>

    <div class="choice-container">
        <h2>Kies uw rol</h2>
        <button onclick="showOptions('kantoorpersoneel')">Kantoorpersoneel</button>
        <button onclick="showOptions('onsite')">On-site Werknemers</button>
    </div>

    <div class="container hidden" id="kantoorpersoneel">
        <div class="section">
            <h2>Kantoorpersoneel - Arbeidsvoorwaarden</h2>
            <p>Hier kunt u arbeidsvoorwaarden kiezen die passen bij uw rol als kantoorpersoneel.</p>

            <h3>Vakantiedagen</h3>
            <div class="option">
                <span>Startbonus: Extra 5 vakantiedagen in het eerste werkjaar</span>
                <span>Kost: € 500</span>
                <button>Kies</button>
            </div>
            <div class="option">
                <span>Gezinsvriendelijke vakantiedagen: 7 extra dagen voor ouders</span>
                <span>Kost: € 700</span>
                <button>Kies</button>
            </div>

            <h3>Pensioenbijdrage</h3>
            <div class="option">
                <span>Flexibele bijdrage: Meer netto salaris door lagere pensioenpremie</span>
                <span>Kost: € 0</span>
                <button>Kies</button>
            </div>
            <div class="option">
                <span>Versnelde pensioenopbouw voor jonge gezinnen</span>
                <span>Kost: € 800</span>
                <button>Kies</button>
            </div>

            <h3>Opleidingsbudget</h3>
            <p>Het opleidingsbudget is aanvullend op het standaard aanbod van de organisatie en wordt extra gefinancierd om persoonlijke ontwikkeling te stimuleren.</p>
            <div class="option">
                <span>Startopleiding: Budget voor professionele cursussen</span>
                <span>Kost: € 1.000</span>
                <button>Kies</button>
            </div>
            <div class="option">
                <span>Training mentorschap en kennisdeling</span>
                <span>Kost: € 600</span>
                <button>Kies</button>
            </div>
        </div>
    </div>

    <div class="container hidden" id="onsite">
        <div class="section">
            <h2>On-site Werknemers - Arbeidsvoorwaarden</h2>
            <p>Hier kunt u arbeidsvoorwaarden kiezen die passen bij uw rol als on-site werknemer.</p>

            <h3>Vakantiedagen</h3>
            <div class="option">
                <span>Sabbatical: 3 maanden onbetaald verlof</span>
                <span>Kost: € 500</span>
                <button>Kies</button>
            </div>
            <div class="option">
                <span>Extra vakantiegeld bovenop reguliere uitkering</span>
                <span>Kost: € 700</span>
                <button>Kies</button>
            </div>

            <h3>Pensioenbijdrage</h3>
            <div class="option">
                <span>Gratis financiële planning voor pensioen</span>
                <span>Kost: € 400</span>
                <button>Kies</button>
            </div>
            <div class="option">
                <span>Extra bijdrage van werkgever in laatste 5 jaar</span>
                <span>Kost: € 900</span>
                <button>Kies</button>
            </div>

            <h3>Opleidingsbudget</h3>
            <p>Het opleidingsbudget is aanvullend op het standaard aanbod van de organisatie en wordt extra gefinancierd om persoonlijke ontwikkeling te stimuleren.</p>
            <div class="option">
                <span>Coachingprogramma’s voor leiderschap</span>
                <span>Kost: € 800</span>
                <button>Kies</button>
            </div>
            <div class="option">
                <span>Training voor vrijwilligerswerk na pensionering</span>
                <span>Kost: € 500</span>
                <button>Kies</button>
            </div>
        </div>
    </div>

    <footer>
        <p>&copy; 2025 Flexibele Arbeidsvoorwaarden Platform. Alle rechten voorbehouden.</p>
    </footer>

    <script>
        function showOptions(role) {
            document.querySelectorAll('.container').forEach(container => {
                container.classList.add('hidden');
            });
            document.getElementById(role).classList.remove('hidden');
        }
    </script>
</body>
</html>
