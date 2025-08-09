<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>52 semaines de M&M</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Dancing Script', 'Brush Script MT', cursive;
            background: linear-gradient(135deg, #a8e6cf 0%, #88d8c0 30%, #7fcdcd 70%, #74b9ff 100%);
            min-height: 100vh;
            color: #2d3436;
            line-height: 1.7;
            position: relative;
        }
        
        body::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><circle cx="20" cy="20" r="2" fill="%23ffffff20"/><circle cx="80" cy="40" r="1.5" fill="%23ffffff30"/><circle cx="40" cy="70" r="1" fill="%23ffffff25"/><circle cx="90" cy="80" r="2.5" fill="%23ffffff20"/><circle cx="10" cy="90" r="1" fill="%23ffffff35"/><circle cx="70" cy="10" r="1.5" fill="%23ffffff25"/></svg>') repeat;
            pointer-events: none;
            z-index: -1;
        }
        
        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 40px 20px;
        }
        
        .header {
            text-align: center;
            margin-bottom: 50px;
        }
        
        .header h1 {
            font-size: 3.5em;
            color: #0984e3;
            margin-bottom: 15px;
            font-weight: 700;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
            transform: rotate(-2deg);
        }
        
        .header p {
            color: #636e72;
            font-size: 1.4em;
            font-weight: 600;
            transform: rotate(1deg);
        }
        
        .week-selector {
            text-align: center;
            margin-bottom: 40px;
        }
        
        .week-selector select {
            padding: 15px 25px;
            font-size: 18px;
            font-family: 'Dancing Script', cursive;
            font-weight: 600;
            border: 3px solid #74b9ff;
            border-radius: 30px;
            background: linear-gradient(45deg, #ffffff, #ddd6fe);
            color: #2d3436;
            cursor: pointer;
            outline: none;
            transition: all 0.3s ease;
            box-shadow: 0 8px 25px rgba(116, 185, 255, 0.3);
            transform: rotate(-1deg);
        }
        
        .week-selector select:hover {
            border-color: #0984e3;
            transform: rotate(1deg) scale(1.05);
            box-shadow: 0 12px 35px rgba(116, 185, 255, 0.4);
        }
        
        .message-card {
            background: linear-gradient(135deg, #ffffff 0%, #a8e6cf 100%);
            padding: 45px;
            border-radius: 30px;
            box-shadow: 0 15px 40px rgba(116, 185, 255, 0.2);
            margin-bottom: 35px;
            transition: all 0.4s ease;
            border: 3px solid #74b9ff;
            transform: rotate(-0.5deg);
            position: relative;
        }
        
        .message-card:hover {
            transform: rotate(0.5deg) translateY(-8px);
            box-shadow: 0 25px 60px rgba(116, 185, 255, 0.3);
            background: linear-gradient(135deg, #ffffff 0%, #88d8c0 100%);
        }
        
        .week-number {
            color: #0984e3;
            font-size: 1.2em;
            text-transform: uppercase;
            letter-spacing: 2px;
            margin-bottom: 20px;
            font-weight: 700;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.1);
        }
        
        .message-text {
            font-size: 1.8em;
            color: #2d3436;
            margin-bottom: 30px;
            font-weight: 600;
            line-height: 1.6;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.05);
        }
        
        .message-photo {
            width: 100%;
            max-width: 400px;
            border-radius: 25px;
            margin: 25px auto;
            display: block;
            box-shadow: 0 10px 30px rgba(116, 185, 255, 0.3);
            border: 4px solid #74b9ff;
            transform: rotate(-1deg);
            transition: all 0.3s ease;
        }
        
        .message-photo:hover {
            transform: rotate(1deg) scale(1.02);
        }
        
        .date {
            text-align: right;
            color: #636e72;
            font-size: 1.1em;
            font-weight: 600;
            border-top: 2px solid #74b9ff;
            padding-top: 20px;
            margin-top: 25px;
        }
        
        .admin-panel {
            background: linear-gradient(135deg, #0984e3 0%, #74b9ff 100%);
            color: white;
            padding: 35px;
            border-radius: 30px;
            margin-top: 50px;
            box-shadow: 0 15px 40px rgba(116, 185, 255, 0.3);
            border: 3px solid #ffffff50;
        }
        
        .admin-panel h3 {
            margin-bottom: 25px;
            color: #ffffff;
            font-size: 1.8em;
            font-weight: 700;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 10px;
            font-weight: 700;
            font-size: 1.2em;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.1);
        }
        
        .form-group input, .form-group textarea {
            width: 100%;
            padding: 15px;
            border: 2px solid #ffffff50;
            border-radius: 20px;
            font-size: 16px;
            font-family: 'Dancing Script', cursive;
            font-weight: 600;
            background: rgba(255, 255, 255, 0.2);
            color: white;
            backdrop-filter: blur(10px);
        }
        
        .form-group input::placeholder, .form-group textarea::placeholder {
            color: #ffffff80;
            font-family: 'Dancing Script', cursive;
        }
        
        .form-group textarea {
            height: 120px;
            resize: vertical;
        }
        
        .btn {
            background: linear-gradient(45deg, #a8e6cf, #88d8c0);
            color: #2d3436;
            padding: 15px 30px;
            border: 2px solid #74b9ff;
            border-radius: 30px;
            cursor: pointer;
            font-size: 18px;
            font-family: 'Dancing Script', cursive;
            font-weight: 700;
            transition: all 0.3s ease;
            margin-right: 15px;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.1);
            box-shadow: 0 5px 15px rgba(116, 185, 255, 0.3);
        }
        
        .btn:hover {
            background: linear-gradient(45deg, #88d8c0, #74b9ff);
            color: white;
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(116, 185, 255, 0.4);
        }
        
        .toggle-admin {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background: linear-gradient(45deg, #0984e3, #74b9ff);
            color: white;
            border: 3px solid #ffffff;
            border-radius: 50%;
            width: 70px;
            height: 70px;
            font-size: 24px;
            cursor: pointer;
            box-shadow: 0 10px 30px rgba(116, 185, 255, 0.4);
            transition: all 0.3s ease;
            animation: pulse 2s infinite;
        }
        
        .toggle-admin:hover {
            transform: scale(1.1) rotate(15deg);
        }
        
        @keyframes pulse {
            0%, 100% { box-shadow: 0 10px 30px rgba(116, 185, 255, 0.4); }
            50% { box-shadow: 0 15px 40px rgba(116, 185, 255, 0.6); }
        }
        
        .hidden {
            display: none;
        }
        
        @media (max-width: 600px) {
            .container {
                padding: 20px 15px;
            }
            
            .header h1 {
                font-size: 2em;
            }
            
            .message-card {
                padding: 25px;
            }
            
            .message-text {
                font-size: 1.1em;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>52 semaines de M&M</h1>
            <p>Une année de petites attentions</p>
        </div>
        
        <div class="week-selector">
            <select id="weekSelect" onchange="showWeek()">
                <option value="current">Semaine actuelle</option>
            </select>
        </div>
        
        <div id="messageContainer">
            <!-- Les messages apparaîtront ici -->
        </div>
        
        <div id="adminPanel" class="admin-panel hidden">
            <h3>✏️ Modifier les messages</h3>
            <div class="form-group">
                <label>Semaine :</label>
                <input type="number" id="adminWeek" min="1" max="52" placeholder="Numéro de semaine (1-52)">
            </div>
            <div class="form-group">
                <label>Message :</label>
                <textarea id="adminMessage" placeholder="Écris ton message..."></textarea>
            </div>
            <div class="form-group">
                <label>Photo (URL ou base64) :</label>
                <input type="text" id="adminPhoto" placeholder="Colle l'URL de ta photo ou laisse vide">
            </div>
            <button class="btn" onclick="saveMessage()">Sauvegarder</button>
            <button class="btn" onclick="loadMessage()">Charger</button>
        </div>
    </div>
    
    <button class="toggle-admin" onclick="toggleAdmin()" title="Mode édition">✏️</button>
    
    <script>
        // Stockage des messages en mémoire
        let messages = {
            1: {
                text: "Mon amour, cette première semaine marque le début de notre année de petits mots. Merci d'être là, tout simplement. ❤️",
                photo: "",
                date: "2025-08-11"
            },
            2: {
                text: "Cette semaine, j'ai pensé à la façon dont tu me regardes le matin. Ça me donne envie de commencer chaque journée avec toi.",
                photo: "",
                date: "2025-08-18"
            },
            3: {
                text: "Merci pour ce café que tu m'as apporté hier soir quand j'étais fatiguée. Ces petites attentions font toute la différence.",
                photo: "",
                date: "2025-08-25"
            }
        };
        
        function getCurrentWeek() {
            const startDate = new Date('2025-08-11'); // Date de début - Lundi 11 août 2025
            const today = new Date();
            const diffTime = today - startDate;
            const diffWeeks = Math.floor(diffTime / (1000 * 60 * 60 * 24 * 7)) + 1;
            return Math.max(1, Math.min(52, diffWeeks));
        }
        
        function initWeekSelector() {
            const select = document.getElementById('weekSelect');
            const currentWeek = getCurrentWeek();
            
            // Ajouter toutes les semaines
            for (let i = 1; i <= 52; i++) {
                const option = document.createElement('option');
                option.value = i;
                option.textContent = `Semaine ${i}`;
                if (i === currentWeek) {
                    option.textContent += ' (actuelle)';
                }
                select.appendChild(option);
            }
            
            // Sélectionner la semaine actuelle
            select.value = 'current';
        }
        
        function showWeek() {
            const select = document.getElementById('weekSelect');
            let weekNumber;
            
            if (select.value === 'current') {
                weekNumber = getCurrentWeek();
            } else {
                weekNumber = parseInt(select.value);
            }
            
            displayMessage(weekNumber);
        }
        
        function displayMessage(weekNumber) {
            const container = document.getElementById('messageContainer');
            const message = messages[weekNumber];
            
            if (message) {
                container.innerHTML = `
                    <div class="message-card">
                        <div class="week-number">Semaine ${weekNumber}</div>
                        <div class="message-text">${message.text}</div>
                        ${message.photo ? `<img src="${message.photo}" alt="Photo de la semaine" class="message-photo">` : ''}
                        <div class="date">${formatDate(message.date)}</div>
                    </div>
                `;
            } else {
                container.innerHTML = `
                    <div class="message-card">
                        <div class="week-number">Semaine ${weekNumber}</div>
                        <div class="message-text">Cette semaine n'a pas encore son message... Patience ! ✨</div>
                        <div class="date">À venir</div>
                    </div>
                `;
            }
        }
        
        function formatDate(dateString) {
            const options = { year: 'numeric', month: 'long', day: 'numeric' };
            return new Date(dateString).toLocaleDateString('fr-FR', options);
        }
        
        function toggleAdmin() {
            const panel = document.getElementById('adminPanel');
            panel.classList.toggle('hidden');
        }
        
        function saveMessage() {
            const week = parseInt(document.getElementById('adminWeek').value);
            const text = document.getElementById('adminMessage').value;
            const photo = document.getElementById('adminPhoto').value;
            
            if (week && text && week >= 1 && week <= 52) {
                messages[week] = {
                    text: text,
                    photo: photo,
                    date: new Date().toISOString().split('T')[0]
                };
                
                alert(`Message pour la semaine ${week} sauvegardé !`);
                
                // Vider les champs
                document.getElementById('adminWeek').value = '';
                document.getElementById('adminMessage').value = '';
                document.getElementById('adminPhoto').value = '';
                
                // Rafraîchir l'affichage si c'est la semaine actuelle
                const currentDisplayed = document.getElementById('weekSelect').value;
                if (currentDisplayed == week || (currentDisplayed === 'current' && week === getCurrentWeek())) {
                    showWeek();
                }
            } else {
                alert('Merci de remplir le numéro de semaine et le message !');
            }
        }
        
        function loadMessage() {
            const week = parseInt(document.getElementById('adminWeek').value);
            if (week && messages[week]) {
                document.getElementById('adminMessage').value = messages[week].text;
                document.getElementById('adminPhoto').value = messages[week].photo || '';
            } else {
                alert('Aucun message trouvé pour cette semaine.');
            }
        }
        
        // Initialisation
        window.onload = function() {
            initWeekSelector();
            showWeek();
        };
    </script>
</body>
</html>
