<!DOCTYPE html>
<html lang="nl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portu Pro</title>
    
    <script src="https://unpkg.com/react@18/umd/react.production.min.js"></script>
    <script src="https://unpkg.com/react-dom@18/umd/react-dom.production.min.js"></script>
    <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
    <script src="https://cdn.tailwindcss.com"></script>

    <script src="https://www.gstatic.com/firebasejs/10.7.1/firebase-app-compat.js"></script>
    <script src="https://www.gstatic.com/firebasejs/10.7.1/firebase-auth-compat.js"></script>
    <script src="https://www.gstatic.com/firebasejs/10.7.1/firebase-firestore-compat.js"></script>

    <link href="https://fonts.googleapis.com/css2?family=Special+Elite&display=swap" rel="stylesheet">
</head>
<body class="bg-[#fdfaf6]">
    <div id="root"></div>

    <script type="text/babel">
        // --- FIREBASE SETUP ---
        // VUL HIER JOUW EIGEN FIREBASE GEGEVENS IN:
        const firebaseConfig = {
            apiKey: "JOUW_API_KEY",
            authDomain: "JOUW_PROJECT.firebaseapp.com",
            projectId: "JOUW_PROJECT_ID",
            storageBucket: "JOUW_PROJECT.appspot.com",
            messagingSenderId: "...",
            appId: "..."
        };

        // Initialiseer Firebase (Compat mode voor browser gebruik)
        firebase.initializeApp(firebaseConfig);
        const auth = firebase.auth();
        const db = firebase.firestore();

        const { useState, useEffect } = React;

        // --- JOUW DATA ---
        const appId = 'port-pro-level-resume-v1';
        const DEFAULT_PINS = { "Robin": "2024", "Isis": "1109", "Yuna": "8822", "Edric": "4590", "Judith": "3312", "Gea": "7765", "Michiel": "9012" };
        const CATS = ['A1', 'A2', 'B1', 'B2', 'C1', 'C2'];
        const ADMIN_SECRET = "115639";
        const UNLOCK_THRESHOLD = 80;
        const QUESTIONS_PER_LEVEL = 40;
        const RAW_VOCAB = {
            A1: [["Olá", "Hallo"], ["Bom dia", "Goedemorgen"], ["Obrigado", "Bedankt"], ["Sim", "Ja"], ["Não", "Nee"], ["Pão", "Brood"], ["Maçã", "Appel"], ["Água", "Water"], ["Leite", "Melk"], ["Café", "Koffie"], ["Mãe", "Moeder"], ["Pai", "Vader"], ["Filho", "Zoon"], ["Filha", "Dochter"], ["Criança", "Kind"], ["Casa", "Huis"], ["Escola", "School"], ["Carro", "Auto"], ["Livro", "Boek"], ["Caneta", "Pen"], ["Cão", "Hond"], ["Gato", "Kat"], ["Amigo", "Vriend"], ["Hoje", "Vandaag"], ["Amanhã", "Morgen"], ["Noite", "Nacht"], ["Dia", "Dag"], ["Hora", "Uur"], ["Minuto", "Minuut"], ["Segundo", "Seconde"], ["Vermelho", "Rood"], ["Azul", "Blauw"], ["Verde", "Groen"], ["Amarelo", "Geel"], ["Preto", "Zwart"], ["Branco", "Wit"], ["Um", "Een"], ["Dois", "Twee"], ["Três", "Drie"], ["Quatro", "Vier"]],
            A2: [["Caminhar", "Wandelen"], ["Correr", "Rennen"], ["Dormir", "Slapen"], ["Comer", "Eten"], ["Beber", "Drinken"], ["Cidade", "Stad"], ["Aldeia", "Dorp"], ["Rua", "Straat"], ["Praia", "Strand"], ["Campo", "Platteland"], ["Quente", "Warm"], ["Frio", "Koud"], ["Grande", "Groot"], ["Pequeno", "Klein"], ["Novo", "Nieuw"], ["Velho", "Oud"], ["Rápido", "Snel"], ["Lento", "Langzaam"], ["Fácil", "Makkelijk"], ["Difícil", "Moeilijk"], ["Feliz", "Gelukkig"], ["Triste", "Droevig"], ["Forte", "Sterk"], ["Fraco", "Zwak"], ["Rico", "Rijk"], ["Pobre", "Arm"], ["Barato", "Goedkoop"], ["Caro", "Duur"], ["Limpo", "Schoon"], ["Sujo", "Vuil"], ["Lindo", "Mooi"], ["Feio", "Lelijk"], ["Aberto", "Open"], ["Fechado", "Gesloten"], ["Perto", "Dichtbij"], ["Longe", "Ver"], ["Antes", "Voorheen"], ["Depois", "Daarna"], ["Sempre", "Altijd"], ["Nunca", "Nooit"]]
        };

        function App() {
            // Hier komt de volledige logica van jouw App functie...
            // (Ik heb de imports hierboven al opgelost voor je)
            
            // [PLAK HIER DE REST VAN JOUW REACT CODE VANAF: const [user, setUser] = useState(null);]
            
            return (
                <div className="p-10 text-center font-black">
                    <h1>Systeem geladen!</h1>
                    <p>Vergeet niet je Firebase Config in te vullen in de code.</p>
                </div>
            );
        }

        const root = ReactDOM.createRoot(document.getElementById('root'));
        root.render(<App />);
    </script>
</body>
</html>
