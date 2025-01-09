<!DOCTYPE html>
<html lang="nl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Arbeidsvoorwaarden op Maat</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f9;
        }
        header {
            background-color: #4CAF50;
            color: white;
            padding: 10px;
            text-align: center;
        }
        nav {
            display: flex;
            justify-content: center;
            background: #ddd;
            padding: 10px;
        }
        nav a {
            margin: 0 10px;
            text-decoration: none;
            color: #333;
            font-weight: bold;
        }
        nav a.active {
            color: #4CAF50;
        }
        .content {
            display: none;
            padding: 20px;
        }
        .content.active {
            display: block;
        }
        .form-group {
            margin-bottom: 15px;
        }
        .form-group label {
            display: block;
            margin-bottom: 5px;
        }
        .form-group select, .form-group button {
            padding: 10px;
            width: 100%;
            max-width: 400px;
        }
        .options {
            margin-top: 20px;
        }
        .lifespan {
            margin-bottom: 20px;
            padding: 10px;
            background: #fff;
            border: 1px solid #ddd;
            border-radius: 5px;
        }
        .lifespan h3 {
            margin-top: 0;
        }
        .token-info {
            margin-top: 20px;
            background: #f9f9f9;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
        }
        .token-info span {
            font-weight: bold;
        }
    </style>
</head>
<body>

<header>
    <h1>Arbeidsvoorwaarden op Maat</h1>
</header>

<nav>
    <a href="#" class="tab-link active" data-tab="tab-choose">Kies Je Rol</a>
    <a href="#" class="tab-link" data-tab="tab-options">Arbeidsvoorwaarden</a>
</nav>

<div id="tab-choose" class="content active">
    <h2>Kies jouw rol</h2>
    <div class="form-group">
        <label for="role">Ben je kantoorpersoneel of on-site medewerker?</label>
        <select id="role">
            <option value="">-- Selecteer een optie --</option>
            <option value="kantoor">Kantoorpersoneel</option>
            <option value="on-site">On-site medewerker</option>
        </select>
    </div>
    <button id="choose-role">Ga verder</button>
</div>

<div id="tab-options" class="content">
    <h2>Arbeidsvoorwaarden</h2>
    <div class="token-info">
        Je hebt <span id="token-count">25</span> tokens. Verdeel deze tokens over de arbeidsvoorwaarden.
    </div>
    <div class="options">
        <div class="lifespan" id="phase-1">
            <h3>1e Levensfase (18-30 jaar)</h3>
            <ul>
                <li>
                    Onbeperkt toegang tot trainingen en cursussen voor persoonlijke groei (<span data-cost="5">5 tokens</span>)
                    <button class="allocate-button" data-phase="1" data-cost="5">Toewijzen</button>
                </li>
                <li>
                    Extra vrije dagen voor studies of examens (<span data-cost="4">4 tokens</span>)
                    <button class="allocate-button" data-phase="1" data-cost="4">Toewijzen</button>
                </li>
                <li>
                    Sportabonnement of wellnessprogramma (<span data-cost="3">3 tokens</span>)
                    <button class="allocate-button" data-phase="1" data-cost="3">Toewijzen</button>
                </li>
                <li>
                    Startbonus of studieleningaflossingsregeling (<span data-cost="6">6 tokens</span>)
                    <button class="allocate-button" data-phase="1" data-cost="6">Toewijzen</button>
                </li>
                <li>
                    Toegang tot betaalbare huisvesting via het bedrijf (<span data-cost="7">7 tokens</span>)
                    <button class="allocate-button" data-phase="1" data-cost="7">Toewijzen</button>
                </li>
                <li id="extra-on-site" style="display: none;">
                    Ondersteuning bij betalen rijbewijs (alleen on-site) (<span data-cost="5">5 tokens</span>)
                    <button class="allocate-button" data-phase="1" data-cost="5">Toewijzen</button>
                </li>
            </ul>
        </div>
        <!-- Herhaal dit voor andere fasen -->
    </div>
</div>

<script>
    const tabs = document.querySelectorAll('.tab-link');
    const contents = document.querySelectorAll('.content');
    const roleSelect = document.getElementById('role');
    const button = document.getElementById('choose-role');
    const extraOnSite = document.getElementById('extra-on-site');
    const tokenCountDisplay = document.getElementById('token-count');
    const allocateButtons = document.querySelectorAll('.allocate-button');

    let remainingTokens = 25;

    tabs.forEach(tab => {
        tab.addEventListener('click', (e) => {
            e.preventDefault();
            tabs.forEach(t => t.classList.remove('active'));
            contents.forEach(c => c.classList.remove('active'));
            tab.classList.add('active');
            document.getElementById(tab.dataset.tab).classList.add('active');
        });
    });

    button.addEventListener('click', () => {
        const role = roleSelect.value;
        if (role === 'on-site') {
            extraOnSite.style.display = 'block';
        } else {
            extraOnSite.style.display = 'none';
        }
        tabs[1].click();
    });

    allocateButtons.forEach(button => {
        button.addEventListener('click', () => {
            const cost = parseInt(button.dataset.cost);
            if (remainingTokens >= cost) {
                remainingTokens -= cost;
                tokenCountDisplay.textContent = remainingTokens;
                button.disabled = true;
                button.textContent = 'Toegewezen';
            } else {
                alert('Niet genoeg tokens beschikbaar!');
            }
        });
    });
</script>

</body>
</html>
