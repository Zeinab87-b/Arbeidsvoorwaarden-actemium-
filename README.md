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
        .content {
            padding: 20px;
        }
        .hidden {
            display: none;
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
        .note {
            margin-bottom: 20px;
            padding: 10px;
            background-color: #fff3cd;
            border: 1px solid #ffeeba;
            border-radius: 5px;
            color: #856404;
        }
    </style>
</head>
<body>

<header>
    <h1>Arbeidsvoorwaarden op Maat</h1>
</header>

<div class="content" id="role-selection">
    <h2>Kies jouw rol</h2>
    <label for="role">Ben je kantoorpersoneel of on-site medewerker?</label>
    <select id="role">
        <option value="">-- Selecteer een optie --</option>
        <option value="kantoor">Kantoorpersoneel</option>
        <option value="on-site">On-site medewerker</option>
    </select>
    <button id="proceed">Ga verder</button>
</div>

<div class="content hidden" id="arbeidsvoorwaarden">
    <div class="note">
        Let op: deze arbeidsvoorwaarden zijn extra en staan los van de arbeidsvoorwaarden die zijn vastgelegd in het CAO Metaal en Techniek.
    </div>
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
                <li id="extra-on-site" class="hidden">
                    Ondersteuning bij betalen rijbewijs (alleen on-site) (<span data-cost="5">5 tokens</span>)
                    <button class="allocate-button" data-phase="1" data-cost="5">Toewijzen</button>
                </li>
            </ul>
        </div>
        <div class="lifespan" id="phase-2">
            <h3>2e Levensfase (30-45 jaar)</h3>
            <ul>
                <li>Betaald ouderschapsverlof (<span data-cost="6">6 tokens</span>)
                    <button class="allocate-button" data-phase="2" data-cost="6">Toewijzen</button>
                </li>
                <li>Kinderopvangtoeslag of samenwerking met kinderopvangcentra (<span data-cost="5">5 tokens</span>)
                    <button class="allocate-button" data-phase="2" data-cost="5">Toewijzen</button>
                </li>
                <li>Aangepaste werktijden voor schoolgaande kinderen (<span data-cost="4">4 tokens</span>)
                    <button class="allocate-button" data-phase="2" data-cost="4">Toewijzen</button>
                </li>
                <li>Zorgverzekering met uitgebreide gezinsdekking (<span data-cost="7">7 tokens</span>)
                    <button class="allocate-button" data-phase="2" data-cost="7">Toewijzen</button>
                </li>
                <li>Sportabonnement (<span data-cost="3">3 tokens</span>)
                    <button class="allocate-button" data-phase="2" data-cost="3">Toewijzen</button>
                </li>
                <li>Korting op gezinsuitjes (<span data-cost="4">4 tokens</span>)
                    <button class="allocate-button" data-phase="2" data-cost="4">Toewijzen</button>
                </li>
                <li>Coaching voor persoonlijke balans (<span data-cost="2">2 tokens</span>)
                    <button class="allocate-button" data-phase="2" data-cost="2">Toewijzen</button>
                </li>
            </ul>
        </div>
        <div class="lifespan" id="phase-3">
            <h3>3e Levensfase (45-55 jaar)</h3>
            <ul>
                <li>Mogelijkheid tot sabbatical (<span data-cost="10">10 tokens</span>)
                    <button class="allocate-button" data-phase="3" data-cost="10">Toewijzen</button>
                </li>
                <li>Extra verlofdagen zonder salarisverlies (<span data-cost="6">6 tokens</span>)
                    <button class="allocate-button" data-phase="3" data-cost="6">Toewijzen</button>
                </li>
                <li>Beloningsprogramma's voor loyaliteit (<span data-cost="4">4 tokens</span>)
                    <button class="allocate-button" data-phase="3" data-cost="4">Toewijzen</button>
                </li>
                <li>Duurzaamheidsinitiatieven, zoals elektrische bedrijfsauto's (<span data-cost="8">8 tokens</span>)
                    <button class="allocate-button" data-phase="3" data-cost="8">Toewijzen</button>
                </li>
            </ul>
        </div>
        <div class="lifespan" id="phase-4">
            <h3>4e Levensfase (55-67 jaar)</h3>
            <ul>
                <li>Versnelde pensioenopbouw (<span data-cost="7">7 tokens</span>)
                    <button class="allocate-button" data-phase="4" data-cost="7">Toewijzen</button>
                </li>
                <li>Gratis financiële planning (<span data-cost="3">3 tokens</span>)
                    <button class="allocate-button" data-phase="4" data-cost="3">Toewijzen</button>
                </li>
                <li>Afbouw van werkuren (<span data-cost="5">5 tokens</span>)
                    <button class="allocate-button" data-phase="4" data-cost="5">Toewijzen</button>
                </li>
                <li>Gezondheidsprogramma's (<span data-cost="6">6 tokens</span>)
                    <button class="allocate-button" data-phase="4" data-cost="6">Toewijzen</button>
                </li>
                <li>Vrijwilligersprogramma's (<span data-cost="2">2 tokens</span>)
                    <button class="allocate-button" data-phase="4" data-cost="2">Toewijzen</button>
                </li>
                <li>Consultancyrollen (<span data-cost="4">4 tokens</span>)
                    <button class="allocate-button" data-phase="4" data-cost="4">Toewijzen</button>
                </li>
            </ul>
        </div>
    </div>
</div>

<script>
    const roleSelection = document.getElementById('role-selection');
    const arbeidsvoorwaarden = document.getElementById('arbeidsvoorwaarden');
    const proceedButton = document.getElementById('proceed');
    const roleSelect = document.getElementById('role');
    const extraOnSite = document.getElementById('extra-on-site');

    proceedButton.addEventListener('click', () => {
        const selectedRole = roleSelect.value;
        if (!selectedRole) {
            alert('Selecteer een rol om verder te gaan.');
            return;
        }

        if (selectedRole === 'on-site') {
            extraOnSite.classList.remove('hidden');
        } else {
            extraOnSite.classList.add('hidden');
        }

        roleSelection.classList.add('hidden');
        arbeidsvoorwaarden.classList.remove('hidden');
    });

    const tokenCountDisplay = document.getElementById('token-count');
    const allocateButtons = document.querySelectorAll('.allocate-button');

    let remainingTokens = 25;

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
