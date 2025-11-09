# Progetto Finale: Sito Completo di Hogwarts

Benvenuto al progetto finale! Qui troverai il codice completo per creare un sito web professionale di Hogwarts con 4 pagine: Home, Case, Materie e Iscrizione.

## 🎯 Obiettivo del Progetto

Creare un sito web multi-pagina completo che include:
- Homepage con hero section e panoramica
- Pagina dedicata alle 4 Case
- Pagina con le Materie insegnate
- Form di iscrizione funzionante
- Navbar uguale su tutte le pagine
- Design responsive e professionale
- Tema Harry Potter coerente

## 📁 Struttura del Progetto

Crea questa struttura di cartelle:

```
hogwarts-sito/
├── index.html
├── case.html
├── materie.html
├── iscrizione.html
└── img/ (opzionale - per immagini)
```

## 🏠 Pagina 1: Homepage (index.html)

La homepage è la prima impressione del tuo sito. Deve essere accogliente e professionale.

### Codice Completo index.html

```html
<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hogwarts - Scuola di Magia e Stregoneria</title>

    <!-- Bootstrap 5.3.3 CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>

    <!-- NAVBAR -->
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark sticky-top">
        <div class="container">
            <a class="navbar-brand" href="index.html">🏰 <strong>Hogwarts</strong></a>

            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>

            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item">
                        <a class="nav-link active" href="index.html">Home</a>
                    </li>
                    <li class="nav-item dropdown">
                        <a class="nav-link dropdown-toggle" href="#" data-bs-toggle="dropdown">
                            Le Case
                        </a>
                        <ul class="dropdown-menu">
                            <li><a class="dropdown-item" href="case.html#grifondoro">🦁 Grifondoro</a></li>
                            <li><a class="dropdown-item" href="case.html#serpeverde">🐍 Serpeverde</a></li>
                            <li><a class="dropdown-item" href="case.html#tassorosso">🦡 Tassorosso</a></li>
                            <li><a class="dropdown-item" href="case.html#corvonero">🦅 Corvonero</a></li>
                            <li><hr class="dropdown-divider"></li>
                            <li><a class="dropdown-item" href="case.html">Tutte le Case</a></li>
                        </ul>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="materie.html">Materie</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="iscrizione.html">Iscrizione</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

    <!-- HERO SECTION -->
    <div class="bg-primary text-white text-center p-5">
        <div class="container">
            <h1 class="display-3">Benvenuto a Hogwarts</h1>
            <p class="lead mb-4">
                La Scuola di Magia e Stregoneria più prestigiosa del mondo
            </p>
            <a href="iscrizione.html" class="btn btn-light btn-lg me-2">📜 Iscriviti Ora</a>
            <a href="case.html" class="btn btn-outline-light btn-lg">🏰 Scopri le Case</a>
        </div>
    </div>

    <!-- SEZIONE CHI SIAMO -->
    <div class="container my-5">
        <div class="row">
            <div class="col-lg-8 mx-auto text-center">
                <h2 class="mb-4">Chi Siamo</h2>
                <p class="lead">
                    Fondata oltre mille anni fa dai quattro maghi più potenti dell'epoca,
                    Hogwarts è il luogo dove generazioni di streghe e maghi hanno imparato
                    l'arte della magia.
                </p>
                <p>
                    Il castello di Hogwarts si trova in Scozia e ospita centinaia di studenti
                    ogni anno, divisi nelle quattro case fondate da Godric Grifondoro,
                    Salazar Serpeverde, Tosca Tassorosso e Corinna Corvonero.
                </p>
            </div>
        </div>
    </div>

    <!-- LE 4 CASE (PREVIEW) -->
    <div class="bg-light py-5">
        <div class="container">
            <h2 class="text-center mb-5">Le Nostre Quattro Case</h2>
            <div class="row g-4">

                <!-- Grifondoro -->
                <div class="col-12 col-sm-6 col-lg-3">
                    <div class="card bg-danger text-white h-100">
                        <div class="card-body text-center">
                            <h1>🦁</h1>
                            <h4 class="card-title">Grifondoro</h4>
                            <p class="card-text">Coraggio e audacia</p>
                            <a href="case.html#grifondoro" class="btn btn-light btn-sm">Scopri</a>
                        </div>
                    </div>
                </div>

                <!-- Serpeverde -->
                <div class="col-12 col-sm-6 col-lg-3">
                    <div class="card bg-success text-white h-100">
                        <div class="card-body text-center">
                            <h1>🐍</h1>
                            <h4 class="card-title">Serpeverde</h4>
                            <p class="card-text">Astuzia e ambizione</p>
                            <a href="case.html#serpeverde" class="btn btn-light btn-sm">Scopri</a>
                        </div>
                    </div>
                </div>

                <!-- Tassorosso -->
                <div class="col-12 col-sm-6 col-lg-3">
                    <div class="card bg-warning h-100">
                        <div class="card-body text-center">
                            <h1>🦡</h1>
                            <h4 class="card-title">Tassorosso</h4>
                            <p class="card-text">Lealtà e pazienza</p>
                            <a href="case.html#tassorosso" class="btn btn-dark btn-sm">Scopri</a>
                        </div>
                    </div>
                </div>

                <!-- Corvonero -->
                <div class="col-12 col-sm-6 col-lg-3">
                    <div class="card bg-primary text-white h-100">
                        <div class="card-body text-center">
                            <h1>🦅</h1>
                            <h4 class="card-title">Corvonero</h4>
                            <p class="card-text">Intelligenza e creatività</p>
                            <a href="case.html#corvonero" class="btn btn-light btn-sm">Scopri</a>
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </div>

    <!-- PERCHE' HOGWARTS -->
    <div class="container my-5">
        <h2 class="text-center mb-5">Perché Scegliere Hogwarts?</h2>
        <div class="row">
            <div class="col-md-4 text-center mb-4">
                <div class="p-3">
                    <h1 class="text-primary">📚</h1>
                    <h5>Insegnamento di Qualità</h5>
                    <p>I migliori professori di magia del mondo insegnano a Hogwarts</p>
                </div>
            </div>
            <div class="col-md-4 text-center mb-4">
                <div class="p-3">
                    <h1 class="text-success">🏰</h1>
                    <h5>Castello Storico</h5>
                    <p>Un ambiente magico e sicuro con oltre 1000 anni di storia</p>
                </div>
            </div>
            <div class="col-md-4 text-center mb-4">
                <div class="p-3">
                    <h1 class="text-warning">✨</h1>
                    <h5>Tradizione Millenaria</h5>
                    <p>Unisciti a generazioni di grandi maghi e streghe</p>
                </div>
            </div>
        </div>
    </div>

    <!-- CALL TO ACTION -->
    <div class="bg-primary text-white text-center py-5">
        <div class="container">
            <h2 class="mb-3">Pronto a Iniziare la Tua Avventura Magica?</h2>
            <p class="lead mb-4">Le ammissioni per l'anno 2024/2025 sono aperte!</p>
            <a href="iscrizione.html" class="btn btn-light btn-lg">📨 Invia la tua Candidatura</a>
        </div>
    </div>

    <!-- FOOTER -->
    <footer class="bg-dark text-white text-center p-4 mt-5">
        <div class="container">
            <p class="mb-1">&copy; 2024 Hogwarts School of Witchcraft and Wizardry</p>
            <p class="mb-0"><small class="text-muted">Draco Dormiens Nunquam Titillandus</small></p>
        </div>
    </footer>

    <!-- Bootstrap JS -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

---

## 🏠 Pagina 2: Le Case (case.html)

Questa pagina mostra informazioni dettagliate su tutte e 4 le case.

### Codice Completo case.html

```html
<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Le Quattro Case - Hogwarts</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>

    <!-- NAVBAR (uguale alla homepage) -->
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark sticky-top">
        <div class="container">
            <a class="navbar-brand" href="index.html">🏰 <strong>Hogwarts</strong></a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item">
                        <a class="nav-link" href="index.html">Home</a>
                    </li>
                    <li class="nav-item dropdown">
                        <a class="nav-link dropdown-toggle active" href="#" data-bs-toggle="dropdown">
                            Le Case
                        </a>
                        <ul class="dropdown-menu">
                            <li><a class="dropdown-item" href="#grifondoro">🦁 Grifondoro</a></li>
                            <li><a class="dropdown-item" href="#serpeverde">🐍 Serpeverde</a></li>
                            <li><a class="dropdown-item" href="#tassorosso">🦡 Tassorosso</a></li>
                            <li><a class="dropdown-item" href="#corvonero">🦅 Corvonero</a></li>
                        </ul>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="materie.html">Materie</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="iscrizione.html">Iscrizione</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

    <!-- HERO -->
    <div class="bg-dark text-white text-center p-5">
        <h1 class="display-4">Le Quattro Case di Hogwarts</h1>
        <p class="lead">Ogni casa rappresenta valori unici e importanti</p>
    </div>

    <div class="container my-5">

        <!-- INTRO -->
        <div class="row mb-5">
            <div class="col-lg-8 mx-auto text-center">
                <p class="lead">
                    Le quattro case di Hogwarts furono fondate dai quattro maghi più potenti
                    dell'epoca. Ogni studente viene smistato dal Cappello Parlante in una
                    delle case in base alle sue qualità personali.
                </p>
            </div>
        </div>

        <!-- GRIFONDORO -->
        <div id="grifondoro" class="mb-5">
            <div class="card bg-danger text-white">
                <div class="card-header">
                    <h2 class="mb-0">🦁 Grifondoro</h2>
                </div>
                <div class="card-body">
                    <div class="row">
                        <div class="col-md-6">
                            <h4>Informazioni</h4>
                            <p><strong>Fondatore:</strong> Godric Grifondoro</p>
                            <p><strong>Valori:</strong> Coraggio, audacia, cavalleria, determinazione</p>
                            <p><strong>Colori:</strong> Rosso scarlatto e oro</p>
                            <p><strong>Animale:</strong> Leone</p>
                            <p><strong>Elemento:</strong> Fuoco</p>
                            <p><strong>Fantasma:</strong> Sir Nicholas de Mimsy (Quasi Senza Testa)</p>
                        </div>
                        <div class="col-md-6">
                            <h4>Studenti Famosi</h4>
                            <ul>
                                <li>Harry Potter</li>
                                <li>Hermione Granger</li>
                                <li>Ron Weasley</li>
                                <li>Albus Silente</li>
                                <li>Minerva McGranitt</li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- SERPEVERDE -->
        <div id="serpeverde" class="mb-5">
            <div class="card bg-success text-white">
                <div class="card-header">
                    <h2 class="mb-0">🐍 Serpeverde</h2>
                </div>
                <div class="card-body">
                    <div class="row">
                        <div class="col-md-6">
                            <h4>Informazioni</h4>
                            <p><strong>Fondatore:</strong> Salazar Serpeverde</p>
                            <p><strong>Valori:</strong> Astuzia, ambizione, ingegno, determinazione</p>
                            <p><strong>Colori:</strong> Verde e argento</p>
                            <p><strong>Animale:</strong> Serpente</p>
                            <p><strong>Elemento:</strong> Acqua</p>
                            <p><strong>Fantasma:</strong> Il Barone Sanguinario</p>
                        </div>
                        <div class="col-md-6">
                            <h4>Studenti Famosi</h4>
                            <ul>
                                <li>Severus Piton</li>
                                <li>Draco Malfoy</li>
                                <li>Horace Lumacorno</li>
                                <li>Bellatrix Lestrange</li>
                                <li>Tom Riddle (Lord Voldemort)</li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- TASSOROSSO -->
        <div id="tassorosso" class="mb-5">
            <div class="card bg-warning">
                <div class="card-header">
                    <h2 class="mb-0">🦡 Tassorosso</h2>
                </div>
                <div class="card-body">
                    <div class="row">
                        <div class="col-md-6">
                            <h4>Informazioni</h4>
                            <p><strong>Fondatore:</strong> Tosca Tassorosso</p>
                            <p><strong>Valori:</strong> Lealtà, dedizione, pazienza, giustizia, onestà</p>
                            <p><strong>Colori:</strong> Giallo e nero</p>
                            <p><strong>Animale:</strong> Tasso</p>
                            <p><strong>Elemento:</strong> Terra</p>
                            <p><strong>Fantasma:</strong> Il Frate Grasso</p>
                        </div>
                        <div class="col-md-6">
                            <h4>Studenti Famosi</h4>
                            <ul>
                                <li>Newt Scamander</li>
                                <li>Cedric Diggory</li>
                                <li>Ninfadora Tonks</li>
                                <li>Pomona Sprite</li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- CORVONERO -->
        <div id="corvonero" class="mb-5">
            <div class="card bg-primary text-white">
                <div class="card-header">
                    <h2 class="mb-0">🦅 Corvonero</h2>
                </div>
                <div class="card-body">
                    <div class="row">
                        <div class="col-md-6">
                            <h4>Informazioni</h4>
                            <p><strong>Fondatore:</strong> Corinna Corvonero</p>
                            <p><strong>Valori:</strong> Intelligenza, creatività, apprendimento, saggezza</p>
                            <p><strong>Colori:</strong> Blu e bronzo</p>
                            <p><strong>Animale:</strong> Aquila</p>
                            <p><strong>Elemento:</strong> Aria</p>
                            <p><strong>Fantasma:</strong> La Dama Grigia (Helena Corvonero)</p>
                        </div>
                        <div class="col-md-6">
                            <h4>Studenti Famosi</h4>
                            <ul>
                                <li>Luna Lovegood</li>
                                <li>Cho Chang</li>
                                <li>Garrick Olivander</li>
                                <li>Filius Vitious</li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- CALL TO ACTION -->
        <div class="alert alert-info text-center">
            <h4>In quale casa saresti smistato?</h4>
            <p class="mb-3">Il Cappello Parlante valuterà le tue qualità durante la cerimonia di smistamento!</p>
            <a href="iscrizione.html" class="btn btn-primary">Iscriviti Ora</a>
        </div>

    </div>

    <!-- FOOTER -->
    <footer class="bg-dark text-white text-center p-4">
        <p class="mb-1">&copy; 2024 Hogwarts School</p>
        <small class="text-muted">Draco Dormiens Nunquam Titillandus</small>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

---

_Continua nella prossima sezione con Materie e Iscrizione..._

## 📚 Pagina 3: Materie (materie.html)

```html
<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Materie - Hogwarts</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>

    <!-- NAVBAR -->
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark sticky-top">
        <div class="container">
            <a class="navbar-brand" href="index.html">🏰 <strong>Hogwarts</strong></a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item"><a class="nav-link" href="index.html">Home</a></li>
                    <li class="nav-item dropdown">
                        <a class="nav-link dropdown-toggle" href="#" data-bs-toggle="dropdown">Le Case</a>
                        <ul class="dropdown-menu">
                            <li><a class="dropdown-item" href="case.html#grifondoro">🦁 Grifondoro</a></li>
                            <li><a class="dropdown-item" href="case.html#serpeverde">🐍 Serpeverde</a></li>
                            <li><a class="dropdown-item" href="case.html#tassorosso">🦡 Tassorosso</a></li>
                            <li><a class="dropdown-item" href="case.html#corvonero">🦅 Corvonero</a></li>
                        </ul>
                    </li>
                    <li class="nav-item"><a class="nav-link active" href="materie.html">Materie</a></li>
                    <li class="nav-item"><a class="nav-link" href="iscrizione.html">Iscrizione</a></li>
                </ul>
            </div>
        </div>
    </nav>

    <!-- HERO -->
    <div class="bg-primary text-white text-center p-5">
        <h1 class="display-4">📚 Le Nostre Materie</h1>
        <p class="lead">Scopri cosa studierai a Hogwarts</p>
    </div>

    <div class="container my-5">

        <div class="alert alert-info mb-5">
            <strong>Nota:</strong> Le seguenti materie sono obbligatorie per i primi 5 anni.
            Dal terzo anno potrai scegliere materie opzionali come Divinazione e Cura delle Creature Magiche.
        </div>

        <div class="row g-4">

            <!-- Pozioni -->
            <div class="col-12 col-md-6 col-lg-4">
                <div class="card h-100">
                    <div class="card-header bg-success text-white">
                        <h4 class="mb-0">🧪 Pozioni</h4>
                    </div>
                    <div class="card-body">
                        <p><strong>Professore:</strong> Severus Piton / Horace Lumacorno</p>
                        <p>Imparerai a preparare pozioni magiche mescolando ingredienti con precisione.
                        Richiede attenzione ai dettagli e pazienza.</p>
                        <span class="badge bg-success">200 studenti</span>
                    </div>
                </div>
            </div>

            <!-- Incantesimi -->
            <div class="col-12 col-md-6 col-lg-4">
                <div class="card h-100">
                    <div class="card-header bg-primary text-white">
                        <h4 class="mb-0">✨ Incantesimi</h4>
                    </div>
                    <div class="card-body">
                        <p><strong>Professore:</strong> Filius Vitious</p>
                        <p>Studia gli incantesimi e impara a lanciare magie con la bacchetta.
                        Da Lumos a Wingardium Leviosa!</p>
                        <span class="badge bg-primary">220 studenti</span>
                    </div>
                </div>
            </div>

            <!-- Trasfigurazione -->
            <div class="col-12 col-md-6 col-lg-4">
                <div class="card h-100">
                    <div class="card-header bg-warning">
                        <h4 class="mb-0">🐈 Trasfigurazione</h4>
                    </div>
                    <div class="card-body">
                        <p><strong>Professore:</strong> Minerva McGranitt</p>
                        <p>Impara a trasformare oggetti e animali. Una delle materie più complesse
                        e affascinanti!</p>
                        <span class="badge bg-warning text-dark">190 studenti</span>
                    </div>
                </div>
            </div>

            <!-- Difesa -->
            <div class="col-12 col-md-6 col-lg-4">
                <div class="card h-100">
                    <div class="card-header bg-danger text-white">
                        <h4 class="mb-0">🛡️ Difesa contro le Arti Oscure</h4>
                    </div>
                    <div class="card-body">
                        <p><strong>Professore:</strong> (cambia ogni anno)</p>
                        <p>Impara a difenderti dalle creature oscure e dalla magia nera.
                        Materia fondamentale per ogni mago!</p>
                        <span class="badge bg-danger">230 studenti</span>
                    </div>
                </div>
            </div>

            <!-- Erbologia -->
            <div class="col-12 col-md-6 col-lg-4">
                <div class="card h-100">
                    <div class="card-header bg-success text-white">
                        <h4 class="mb-0">🌿 Erbologia</h4>
                    </div>
                    <div class="card-body">
                        <p><strong>Professore:</strong> Pomona Sprite</p>
                        <p>Studia le piante magiche e le loro proprietà. Le lezioni si tengono
                        nelle serre del castello.</p>
                        <span class="badge bg-success">180 studenti</span>
                    </div>
                </div>
            </div>

            <!-- Volo -->
            <div class="col-12 col-md-6 col-lg-4">
                <div class="card h-100">
                    <div class="card-header bg-info text-white">
                        <h4 class="mb-0">🧹 Volo</h4>
                    </div>
                    <div class="card-body">
                        <p><strong>Professore:</strong> Rolanda Bumb</p>
                        <p>Impara a volare sulla scopa magica! Materia solo per il primo anno,
                        poi si gioca a Quidditch!</p>
                        <span class="badge bg-info">150 studenti</span>
                    </div>
                </div>
            </div>

        </div>

        <!-- Materie Opzionali -->
        <div class="mt-5">
            <h2 class="text-center mb-4">Materie Opzionali (dal 3° anno)</h2>
            <div class="row">
                <div class="col-md-4 mb-3">
                    <div class="border p-3 text-center">
                        <h5>🔮 Divinazione</h5>
                        <p>Predici il futuro con sfere di cristallo e foglie di tè</p>
                    </div>
                </div>
                <div class="col-md-4 mb-3">
                    <div class="border p-3 text-center">
                        <h5>🦄 Cura delle Creature Magiche</h5>
                        <p>Impara a prenderti cura di creature magiche</p>
                    </div>
                </div>
                <div class="col-md-4 mb-3">
                    <div class="border p-3 text-center">
                        <h5>🔢 Aritmanzia</h5>
                        <p>Studia le proprietà magiche dei numeri</p>
                    </div>
                </div>
            </div>
        </div>

    </div>

    <!-- FOOTER -->
    <footer class="bg-dark text-white text-center p-4 mt-5">
        <p class="mb-1">&copy; 2024 Hogwarts School</p>
        <small class="text-muted">Draco Dormiens Nunquam Titillandus</small>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

---

## 📝 Pagina 4: Iscrizione (iscrizione.html)

```html
<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Iscrizione - Hogwarts</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>

    <!-- NAVBAR -->
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark sticky-top">
        <div class="container">
            <a class="navbar-brand" href="index.html">🏰 <strong>Hogwarts</strong></a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item"><a class="nav-link" href="index.html">Home</a></li>
                    <li class="nav-item dropdown">
                        <a class="nav-link dropdown-toggle" href="#" data-bs-toggle="dropdown">Le Case</a>
                        <ul class="dropdown-menu">
                            <li><a class="dropdown-item" href="case.html#grifondoro">🦁 Grifondoro</a></li>
                            <li><a class="dropdown-item" href="case.html#serpeverde">🐍 Serpeverde</a></li>
                            <li><a class="dropdown-item" href="case.html#tassorosso">🦡 Tassorosso</a></li>
                            <li><a class="dropdown-item" href="case.html#corvonero">🦅 Corvonero</a></li>
                        </ul>
                    </li>
                    <li class="nav-item"><a class="nav-link" href="materie.html">Materie</a></li>
                    <li class="nav-item"><a class="nav-link active" href="iscrizione.html">Iscrizione</a></li>
                </ul>
            </div>
        </div>
    </nav>

    <!-- HERO -->
    <div class="bg-primary text-white text-center p-5">
        <h1 class="display-4">📜 Modulo di Iscrizione</h1>
        <p class="lead">Compila il modulo per richiedere l'ammissione a Hogwarts</p>
    </div>

    <div class="container my-5">
        <div class="row">
            <div class="col-lg-8 mx-auto">

                <div class="alert alert-success">
                    <strong>Ammissioni Aperte!</strong> Le iscrizioni per l'anno scolastico 2024/2025 sono aperte.
                </div>

                <form class="border p-4 rounded bg-light">

                    <!-- DATI PERSONALI -->
                    <h3 class="mb-4">📋 Dati Personali</h3>

                    <div class="mb-3">
                        <label for="nome" class="form-label">Nome completo *</label>
                        <input type="text" class="form-control" id="nome" name="nome"
                               placeholder="Es: Harry Potter" required>
                    </div>

                    <div class="mb-3">
                        <label for="email" class="form-label">Email *</label>
                        <input type="email" class="form-control" id="email" name="email"
                               placeholder="harry@hogwarts.com" required>
                    </div>

                    <div class="row">
                        <div class="col-md-6 mb-3">
                            <label for="nascita" class="form-label">Data di nascita</label>
                            <input type="date" class="form-control" id="nascita" name="nascita">
                        </div>
                        <div class="col-md-6 mb-3">
                            <label for="eta" class="form-label">Età *</label>
                            <input type="number" class="form-control" id="eta" name="eta"
                                   min="11" max="17" placeholder="11" required>
                        </div>
                    </div>

                    <hr class="my-4">

                    <!-- PREFERENZA CASA -->
                    <h3 class="mb-3">🏠 Preferenza Casa</h3>
                    <p>In quale casa vorresti essere smistato? (Il Cappello Parlante deciderà definitivamente)</p>

                    <div class="form-check">
                        <input class="form-check-input" type="radio" name="casa" id="grifondoro" value="grifondoro">
                        <label class="form-check-label" for="grifondoro">
                            🦁 <strong>Grifondoro</strong> - Coraggio e audacia
                        </label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" name="casa" id="serpeverde" value="serpeverde">
                        <label class="form-check-label" for="serpeverde">
                            🐍 <strong>Serpeverde</strong> - Astuzia e ambizione
                        </label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="radio" name="casa" id="tassorosso" value="tassorosso">
                        <label class="form-check-label" for="tassorosso">
                            🦡 <strong>Tassorosso</strong> - Lealtà e pazienza
                        </label>
                    </div>
                    <div class="form-check mb-3">
                        <input class="form-check-input" type="radio" name="casa" id="corvonero" value="corvonero">
                        <label class="form-check-label" for="corvonero">
                            🦅 <strong>Corvonero</strong> - Intelligenza e creatività
                        </label>
                    </div>

                    <hr class="my-4">

                    <!-- MATERIE -->
                    <h3 class="mb-3">📚 Materie di Interesse</h3>
                    <p>Seleziona le materie che ti interessano di più:</p>

                    <div class="form-check">
                        <input class="form-check-input" type="checkbox" id="pozioni" name="materie" value="pozioni">
                        <label class="form-check-label" for="pozioni">Pozioni</label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="checkbox" id="incantesimi" name="materie" value="incantesimi">
                        <label class="form-check-label" for="incantesimi">Incantesimi</label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="checkbox" id="trasfigurazione" name="materie" value="trasfigurazione">
                        <label class="form-check-label" for="trasfigurazione">Trasfigurazione</label>
                    </div>
                    <div class="form-check">
                        <input class="form-check-input" type="checkbox" id="difesa" name="materie" value="difesa">
                        <label class="form-check-label" for="difesa">Difesa contro le Arti Oscure</label>
                    </div>
                    <div class="form-check mb-3">
                        <input class="form-check-input" type="checkbox" id="erbologia" name="materie" value="erbologia">
                        <label class="form-check-label" for="erbologia">Erbologia</label>
                    </div>

                    <hr class="my-4">

                    <!-- ANNO -->
                    <h3 class="mb-3">📅 Anno di Corso</h3>

                    <div class="mb-3">
                        <label for="anno" class="form-label">Seleziona anno *</label>
                        <select class="form-select" id="anno" name="anno" required>
                            <option value="">-- Scegli --</option>
                            <option value="1">Primo Anno</option>
                            <option value="2">Secondo Anno</option>
                            <option value="3">Terzo Anno</option>
                            <option value="4">Quarto Anno</option>
                            <option value="5">Quinto Anno</option>
                        </select>
                    </div>

                    <hr class="my-4">

                    <!-- MOTIVAZIONE -->
                    <h3 class="mb-3">✍️ Motivazione</h3>

                    <div class="mb-3">
                        <label for="motivazione" class="form-label">
                            Perché vuoi frequentare Hogwarts?
                        </label>
                        <textarea class="form-control" id="motivazione" name="motivazione"
                                  rows="5" placeholder="Scrivi qui le tue motivazioni..."></textarea>
                    </div>

                    <hr class="my-4">

                    <!-- PRIVACY -->
                    <h3 class="mb-3">🔒 Privacy e Consenso</h3>

                    <div class="form-check mb-4">
                        <input class="form-check-input" type="checkbox" id="privacy" name="privacy" required>
                        <label class="form-check-label" for="privacy">
                            Accetto che i miei dati siano utilizzati dal Ministero della Magia
                            per finalità didattiche *
                        </label>
                    </div>

                    <!-- PULSANTI -->
                    <div class="d-grid gap-2 d-md-flex">
                        <button type="submit" class="btn btn-primary btn-lg">
                            📨 Invia Candidatura
                        </button>
                        <button type="reset" class="btn btn-secondary btn-lg">
                            🗑️ Cancella Tutto
                        </button>
                    </div>

                    <p class="mt-3"><small class="text-muted">* Campi obbligatori</small></p>

                </form>

            </div>
        </div>
    </div>

    <!-- FOOTER -->
    <footer class="bg-dark text-white text-center p-4 mt-5">
        <p class="mb-1">&copy; 2024 Hogwarts School</p>
        <small class="text-muted">Draco Dormiens Nunquam Titillandus</small>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

---

## ✅ Checklist Completa Progetto

Usa questa checklist per verificare di aver completato tutto:

### Struttura e File
- [ ] Cartella `hogwarts-sito` creata
- [ ] `index.html` creato
- [ ] `case.html` creato
- [ ] `materie.html` creato
- [ ] `iscrizione.html` creato

### Bootstrap e HTML
- [ ] Bootstrap CDN incluso in tutte le pagine
- [ ] Tutti i file hanno DOCTYPE e meta viewport
- [ ] Codice HTML valido (testa su validator.w3.org)
- [ ] Tutti i tag chiusi correttamente

### Navbar
- [ ] Navbar uguale su tutte le 4 pagine
- [ ] Logo "Hogwarts" funzionante
- [ ] Menu con Home, Le Case (dropdown), Materie, Iscrizione
- [ ] Link evidenziato sulla pagina corrente (active)
- [ ] Hamburger menu funziona su mobile

### Homepage (index.html)
- [ ] Hero section con titolo e pulsanti
- [ ] Sezione "Chi Siamo"
- [ ] Card delle 4 case responsive
- [ ] Sezione "Perché Hogwarts"
- [ ] Call to action finale
- [ ] Footer

### Pagina Case (case.html)
- [ ] Informazioni complete per tutte e 4 le case
- [ ] Card con colori appropriati per ogni casa
- [ ] Studenti famosi elencati
- [ ] Ancore funzionanti (#grifondoro, ecc.)

### Pagina Materie (materie.html)
- [ ] Almeno 6 materie mostrate in card
- [ ] Grid responsive (3 colonne desktop, 2 tablet, 1 mobile)
- [ ] Sezione materie opzionali
- [ ] Badge con numero studenti

### Pagina Iscrizione (iscrizione.html)
- [ ] Form completo e funzionante
- [ ] Tutti i tipi di input (text, email, date, number, radio, checkbox, select, textarea)
- [ ] Campi obbligatori marcati
- [ ] Pulsanti submit e reset
- [ ] Checkbox privacy obbligatorio

### Responsive
- [ ] Testato su mobile (telefono)
- [ ] Testato su tablet
- [ ] Testato su desktop
- [ ] Navbar collassa su mobile
- [ ] Grid si adatta ai diversi schermi

### Design e UX
- [ ] Colori coerenti tema Harry Potter
- [ ] Spaziature adeguate
- [ ] Testi leggibili
- [ ] Link tutti funzionanti
- [ ] Footer su tutte le pagine

## 🚀 Come Testare

1. **Test Locale**:
   - Apri ogni pagina con Live Server
   - Clicca tutti i link
   - Compila e invia il form
   - Ridimensiona la finestra per testare responsive

2. **Test Mobile**:
   - F12 > Device Toolbar
   - Testa iPhone, iPad, Android
   - Verifica hamburger menu
   - Controlla che tutto sia leggibile

3. **Validazione HTML**:
   - Vai su [validator.w3.org](https://validator.w3.org)
   - Carica ogni file HTML
   - Correggi eventuali errori

## 🎨 Personalizzazioni Opzionali

Se vuoi andare oltre:
- Aggiungi immagini (cerca su Unsplash, Pexels)
- Aggiungi icone (Font Awesome, Bootstrap Icons)
- Crea una pagina "Professori"
- Aggiungi animazioni CSS
- Crea una galleria foto del castello
- Aggiungi Google Maps per la posizione di Hogwarts

## 🏆 Hai Finito!

Congratulazioni! 🎉 Hai completato il progetto finale!

Ora puoi:
1. **Pubblicare** il sito su GitHub Pages, Netlify o Vercel
2. **Condividere** con amici e famiglia
3. **Aggiungere** al tuo portfolio
4. **Continuare** ad imparare: JavaScript, React, Backend...

---

*"È nelle nostre scelte che dimostriamo chi siamo veramente."* - Albus Silente

Hai scelto di imparare il Web Development. Benvenuto nel mondo della programmazione! 🪄💻✨
