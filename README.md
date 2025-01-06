# Arbeidsvoorwaarden-actemium-
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
        .link {
            text-align: center;
            margin: 2rem 0;
        }
        .link a {
            text-decoration: none;
            color: white;
            background-color: #0073e6;
            padding: 0.75rem 1.5rem;
            border-radius: 5px;
            font-size: 1rem;
        }
        .link a:hover {
            background-color: #005bb5;
        }
    </style>
</head>
<body>
    <header>
        <h1>Flexibele Arbeidsvoorwaarden</h1>
    </header>

    <div class="container">
        <!-- Budget Section -->
        <div class="section">
            <h2>Uw Budget</h2>
            <p>Beschikbaar budget: <strong>€ 2.500</strong></p>
        </div>

        <!-- Vakantiedagen Section -->
        <div class="section">
            <h2>Vakantiedagen</h2>
            <div class="option">
                <span>5 extra vakantiedagen</span>
                <span>Kost: € 500</span>
                <button>Kies</button>
            </div>
            <div class="option">
                <span>Geen extra vakantiedagen</span>
                <span>Kost: € 0</span>
                <button>Kies</button>
            </div>
        </div>

        <!-- Pensioen Section -->
        <div class="section">
            <h2>Pensioenbijdrage</h2>
            <div class="option">
                <span>Verhoog bijdrage met 5%</span>
                <span>Kost: € 750</span>
                <button>Kies</button>
            </div>
            <div class="option">
                <span>Standaard bijdrage</span>
                <span>Kost: € 0</span>
                <button>Kies</button>
            </div>
        </div>

        <!-- Opleidingsbudget Section -->
        <div class="section">
            <h2>Opleidingsbudget</h2>
            <div class="option">
                <span>Extra € 1.000 voor opleidingen</span>
                <span>Kost: € 1.000</span>
                <button>Kies</button>
            </div>
            <div class="option">
                <span>Geen extra budget</span>
                <span>Kost: € 0</span>
                <button>Kies</button>
            </div>
        </div>

        <!-- Link Section -->
        <div class="link">
            <a href="#">Ga naar uw persoonlijke dashboard</a>
        </div>
    </div>

    <footer>
        <p>&copy; 2025 Flexibele Arbeidsvoorwaarden Platform. Alle rechten voorbehouden.</p>
    </footer>
</body>
</html>
