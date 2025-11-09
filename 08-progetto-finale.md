# Lezione 8: Progetto Finale - Metti Tutto Insieme!

Benvenuto all'ultima lezione! Oggi è il giorno di applicare **tutto quello che hai imparato** per creare un sito web completo. Sei pronto a costruire il sito ufficiale di Hogwarts?

## 🎯 Obiettivi della Lezione

Alla fine di questa lezione saprai:
- Pianificare un progetto web dall'inizio
- Strutturare file e cartelle
- Combinare HTML, Bootstrap e tutti i componenti
- Creare un sito multi-pagina completo
- Pubblicare il tuo lavoro online

## 🧙 Preparazione al Progetto

### Cosa Costruirai

Un **sito web completo di Hogwarts** con:
- Homepage con hero section
- Pagina delle 4 Case
- Pagina Materie
- Form di iscrizione
- Menu di navigazione funzionante
- Design responsive
- Componenti Bootstrap professionali

### Struttura del Progetto

Prima di iniziare, crea questa struttura:

```
hogwarts-website/
├── index.html          # Homepage
├── case.html           # Pagina Case
├── materie.html        # Pagina Materie
├── iscrizione.html     # Form iscrizione
├── css/
│   └── style.css       # (opzionale) CSS custom
└── img/
    └── (immagini)
```

### Checklist Pre-Progetto

Prima di partire, assicurati di avere:
- [ ] Visual Studio Code aperto
- [ ] Live Server installato
- [ ] Creata cartella `hogwarts-website`
- [ ] Connessione Internet (per Bootstrap CDN)
- [ ] Voglia di programmare!

## 🎨 Homepage - index.html

La homepage è la prima pagina che vedono i visitatori.

**Sezioni da includere:**
1. Navbar con link alle altre pagine
2. Hero section con titolo grande e pulsante
3. Sezione "Benvenuto" con testo
4. Griglia con le 4 case (card)
5. Sezione "Perché Hogwarts"
6. Footer

**Esempio struttura:**

```html
<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hogwarts - Scuola di Magia</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>

    <!-- Navbar -->
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
        <div class="container">
            <a class="navbar-brand" href="index.html">🏰 Hogwarts</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item">
                        <a class="nav-link active" href="index.html">Home</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="case.html">Le Case</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="materie.html">Materie</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="iscrizione.html">Iscriviti</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <div class="bg-primary text-white text-center p-5">
        <div class="container">
            <h1 class="display-4">Benvenuto a Hogwarts</h1>
            <p class="lead">La Scuola di Magia e Stregoneria più prestigiosa del mondo</p>
            <a href="iscrizione.html" class="btn btn-light btn-lg mt-3">📜 Iscriviti Ora</a>
        </div>
    </div>

    <!-- Sezione Benvenuto -->
    <div class="container my-5">
        <div class="row">
            <div class="col-lg-8 mx-auto text-center">
                <h2>Chi Siamo</h2>
                <p class="lead">
                    Fondata oltre mille anni fa da quattro grandi maghi, Hogwarts è il luogo
                    dove generazioni di streghe e maghi hanno imparato l'arte della magia.
                </p>
            </div>
        </div>
    </div>

    <!-- Le 4 Case (Card Grid) -->
    <div class="bg-light py-5">
        <div class="container">
            <h2 class="text-center mb-5">Le Nostre Quattro Case</h2>
            <div class="row g-4">
                <!-- Inserisci qui le 4 card delle case -->
                <!-- Vedi lezioni precedenti per esempi -->
            </div>
        </div>
    </div>

    <!-- Perché Hogwarts -->
    <div class="container my-5">
        <h2 class="text-center mb-4">Perché Scegliere Hogwarts?</h2>
        <div class="row">
            <div class="col-md-4 text-center mb-4">
                <h3>📚</h3>
                <h5>Migliori Professori</h5>
                <p>Insegnanti esperti e maghi rinomati</p>
            </div>
            <div class="col-md-4 text-center mb-4">
                <h3>🏰</h3>
                <h5>Castello Storico</h5>
                <p>Un ambiente magico e sicuro</p>
            </div>
            <div class="col-md-4 text-center mb-4">
                <h3>✨</h3>
                <h5>Tradizione Millenaria</h5>
                <p>Oltre 1000 anni di eccellenza</p>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <div class="bg-dark text-white text-center p-4">
        <p class="mb-0">&copy; 2024 Hogwarts School of Witchcraft and Wizardry</p>
        <small>Draco Dormiens Nunquam Titillandus</small>
    </div>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

## 🏰 Pagina Case - case.html

**Cosa includere:**
1. Stessa navbar (copia-incolla)
2. Header pagina
3. Descrizione dettagliata di ogni casa
4. Informazioni su fondatori, valori, colori
5. Lista studenti famosi
6. Footer (copia-incolla)

## 📚 Pagina Materie - materie.html

**Cosa includere:**
1. Navbar
2. Hero section "Le Nostre Materie"
3. Card per ogni materia (minimo 6):
   - Pozioni
   - Incantesimi
   - Trasfigurazione
   - Difesa contro le Arti Oscure
   - Erbologia
   - Volo
4. Layout grid responsive
5. Footer

## 📝 Pagina Iscrizione - iscrizione.html

**Cosa includere:**
1. Navbar
2. Titolo "Iscriviti a Hogwarts"
3. Form completo con:
   - Dati personali (nome, email, età, data nascita)
   - Scelta casa (radio button)
   - Materie preferite (checkbox)
   - Anno di corso (select)
   - Motivazione (textarea)
   - Privacy checkbox
   - Pulsanti invia/reset
4. Alert informativi
5. Footer

## 🎯 Checklist Progetto Completo

### HTML e Struttura
- [ ] 4 pagine HTML create
- [ ] Navbar uguale su tutte le pagine
- [ ] Footer uguale su tutte le pagine
- [ ] Link tra pagine funzionanti
- [ ] Tutti i tag chiusi correttamente

### Bootstrap e Design
- [ ] Bootstrap CDN incluso in tutte le pagine
- [ ] Container usati correttamente
- [ ] Grid system per layout
- [ ] Card per contenuti
- [ ] Bottoni con classi Bootstrap
- [ ] Colori consistenti (tema Harry Potter)

### Responsive
- [ ] Meta viewport in tutte le pagine
- [ ] Navbar collassa su mobile
- [ ] Grid responsive (col-12 col-md-6 col-lg-3, ecc.)
- [ ] Padding/margin responsive
- [ ] Testato su mobile e desktop

### Contenuti
- [ ] Testi completi e corretti
- [ ] Titoli gerarchici (h1, h2, h3)
- [ ] Immagini con alt text (se usate)
- [ ] Form funzionante e completo
- [ ] Tema Harry Potter coerente

### Qualità Codice
- [ ] Codice indentato bene
- [ ] Commenti dove necessario
- [ ] Nomi file in minuscolo
- [ ] No errori in console browser

## 💡 Tips per il Progetto

### 1. Copia e Modifica

Non reinventare la ruota! Copia:
- La navbar da una pagina all'altra
- Il footer da una pagina all'altra
- Componenti dalle lezioni precedenti

### 2. Lavora per Sezioni

Non fare tutto insieme:
1. Prima fai navbar + footer su tutte le pagine
2. Poi completa index.html
3. Poi case.html
4. Poi materie.html
5. Infine iscrizione.html

### 3. Salva Spesso

Premi `Ctrl+S` ogni volta che fai una modifica!

### 4. Testa Sempre

Apri con Live Server e controlla dopo ogni modifica.

### 5. Validazione HTML

Vai su [validator.w3.org](https://validator.w3.org) e controlla il tuo HTML.

## 🚀 Come Pubblicare il Sito

Una volta finito, puoi pubblicare il tuo sito gratuitamente!

### Opzione 1: GitHub Pages

1. Crea account su [github.com](https://github.com)
2. Crea un nuovo repository "hogwarts-website"
3. Carica tutti i file
4. Vai su Settings > Pages
5. Abilita GitHub Pages
6. Il tuo sito sarà su `tuousername.github.io/hogwarts-website`

### Opzione 2: Netlify

1. Vai su [netlify.com](https://www.netlify.com)
2. Trascina la cartella del progetto
3. Netlify pubblicherà il sito automaticamente
4. Riceverai un link tipo `random-name.netlify.app`

### Opzione 3: Vercel

1. Vai su [vercel.com](https://vercel.com)
2. Importa il progetto
3. Deploy automatico

## 🏆 Challenge Finale

**Crea il sito completo di Hogwarts con tutti i requisiti!**

Quando hai finito:
1. Testa su mobile e desktop
2. Controlla che tutti i link funzionino
3. Valida l'HTML
4. Pubblica online
5. Condividi il link con amici e famiglia!

## ⭐ Bonus - Funzionalità Extra (Opzionali)

Se vuoi andare oltre, aggiungi:
- [ ] Pagina "Professori" con foto e descrizioni
- [ ] Pagina "Storia" con timeline di Hogwarts
- [ ] Galleria immagini del castello
- [ ] Video YouTube incorporato
- [ ] Mappa interattiva (Google Maps)
- [ ] Sezione News/Blog
- [ ] Dark mode (toggle chiaro/scuro)
- [ ] Animazioni CSS
- [ ] Form che invia email (con servizi tipo Formspree)

## 📚 Risorse Finali

- [Bootstrap Docs](https://getbootstrap.com/docs/5.3)
- [MDN Web Docs](https://developer.mozilla.org)
- [W3Schools](https://www.w3schools.com)
- [Stack Overflow](https://stackoverflow.com) - Per domande

## ✅ Hai Finito?

Congratulazioni! 🎉

Se hai completato il progetto:
- ✅ Conosci HTML
- ✅ Sai usare Bootstrap 5
- ✅ Sai creare siti responsive
- ✅ Hai pubblicato il tuo primo sito web!

## 🎯 Prossimi Passi nel Tuo Percorso

Ora che hai le basi, puoi imparare:
1. **CSS avanzato** - Animazioni, flexbox, grid CSS
2. **JavaScript** - Rendere il sito interattivo
3. **Frameworks JS** - React, Vue, Angular
4. **Backend** - Node.js, Python, PHP
5. **Database** - MySQL, MongoDB

### Progetti da Provare

- Portfolio personale
- Blog
- E-commerce
- Dashboard
- Landing page per un'attività
- Clone di siti famosi (Netflix, Spotify, ecc.)

## 🌟 Messaggio Finale

Hai completato il corso! Sei partito da zero e ora sai creare siti web completi.

**Ricorda:**
- La pratica è fondamentale
- Sbagliare è normale (anche i migliori sbagliano!)
- Continua a imparare e sperimentare
- Diventa parte della community (forum, Discord, ecc.)

---

*"Sono le nostre scelte, Harry, che dimostrano chi siamo veramente, molto più che le nostre capacità."* - Albus Silente

Hai **scelto** di imparare la programmazione web. Questa è solo l'inizio della tua avventura nel mondo del Web Development!

**Buona fortuna e buon coding!** 🪄💻✨

---

Per il progetto finale dettagliato con codice completo, vai a [progetti/progetto-finale.md](progetti/progetto-finale.md)
