# Lezione 6: Bootstrap Componenti - Card, Navbar e Altro

Benvenuto alla sesta lezione! Oggi scoprirai i componenti pronti di Bootstrap: card, navbar, alert, modal e molto altro. Sono come incantesimi già pronti!

## 🎯 Obiettivi della Lezione

Alla fine di questa lezione saprai:
- Creare card bellissime per contenuti
- Costruire una navbar (menu di navigazione)
- Usare alert, badge e button group
- Implementare modal (finestre popup)
- Combinare componenti per siti professionali

## 🧙 Concetti Fondamentali

### Cosa sono i Componenti?

I **componenti Bootstrap** sono pezzi di interfaccia già pronti che puoi copiare e personalizzare:
- Card = Box per contenuti
- Navbar = Menu di navigazione
- Alert = Messaggi di avviso
- Modal = Finestre popup
- Badge = Etichette numerate
- E molti altri!

## ⚡ Analogia Harry Potter

I componenti Bootstrap sono come **oggetti magici già incantati**:
- **Card** = Carte Cioccorane (contengono informazioni)
- **Navbar** = Mappa del Malandrino (ti fa navigare)
- **Alert** = Strillone (ti avvisa di qualcosa)
- **Modal** = Pensatoio (apre una finestra su altro)
- **Badge** = Distintivi Prefetti (etichette speciali)

Invece di creare questi oggetti da zero, usi quelli già pronti!

## 🃏 Card - Box per Contenuti

Le **card** sono box rettangolari perfetti per mostrare contenuti.

### Card Base

```html
<div class="card">
    <div class="card-body">
        <h5 class="card-title">Titolo Card</h5>
        <p class="card-text">Contenuto della card.</p>
        <a href="#" class="btn btn-primary">Vai</a>
    </div>
</div>
```

### Card con Immagine

```html
<div class="card" style="width: 18rem;">
    <img src="hogwarts.jpg" class="card-img-top" alt="Hogwarts">
    <div class="card-body">
        <h5 class="card-title">Castello di Hogwarts</h5>
        <p class="card-text">La scuola di magia più famosa del mondo.</p>
        <a href="#" class="btn btn-primary">Scopri di più</a>
    </div>
</div>
```

### Card con Header e Footer

```html
<div class="card">
    <div class="card-header">
        Header della Card
    </div>
    <div class="card-body">
        <h5 class="card-title">Titolo</h5>
        <p class="card-text">Contenuto principale.</p>
    </div>
    <div class="card-footer text-muted">
        Footer della card
    </div>
</div>
```

### Card Colorate

```html
<div class="card text-white bg-primary mb-3">
    <div class="card-body">
        <h5 class="card-title">Card Blu</h5>
        <p class="card-text">Sfondo blu.</p>
    </div>
</div>

<div class="card text-white bg-success mb-3">
    <div class="card-body">
        <h5 class="card-title">Card Verde</h5>
        <p class="card-text">Sfondo verde.</p>
    </div>
</div>
```

## 🧭 Navbar - Menu di Navigazione

La **navbar** è il menu in alto del sito.

### Navbar Base

```html
<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <div class="container-fluid">
        <a class="navbar-brand" href="#">Hogwarts</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav">
                <li class="nav-item">
                    <a class="nav-link active" href="#">Home</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">Case</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">Materie</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">Contatti</a>
                </li>
            </ul>
        </div>
    </div>
</nav>
```

**Parti importanti:**
- `navbar-dark bg-dark` = Navbar scura
- `navbar-expand-lg` = Si espande su schermi grandi
- `navbar-toggler` = Pulsante hamburger per mobile
- `collapse` = Contenuto che si nasconde su mobile

### Navbar con Dropdown

```html
<nav class="navbar navbar-expand-lg navbar-light bg-light">
    <div class="container-fluid">
        <a class="navbar-brand" href="#">Hogwarts</a>
        <div class="collapse navbar-collapse">
            <ul class="navbar-nav">
                <li class="nav-item dropdown">
                    <a class="nav-link dropdown-toggle" href="#" data-bs-toggle="dropdown">
                        Case
                    </a>
                    <ul class="dropdown-menu">
                        <li><a class="dropdown-item" href="#">Grifondoro</a></li>
                        <li><a class="dropdown-item" href="#">Serpeverde</a></li>
                        <li><a class="dropdown-item" href="#">Tassorosso</a></li>
                        <li><a class="dropdown-item" href="#">Corvonero</a></li>
                    </ul>
                </li>
            </ul>
        </div>
    </div>
</nav>
```

## 🚨 Alert - Messaggi di Avviso

```html
<div class="alert alert-primary">Messaggio informativo</div>
<div class="alert alert-success">Operazione riuscita!</div>
<div class="alert alert-warning">Attenzione!</div>
<div class="alert alert-danger">Errore!</div>
<div class="alert alert-info">Info importante</div>
```

### Alert Chiudibile

```html
<div class="alert alert-warning alert-dismissible fade show">
    <strong>Attenzione!</strong> Questo messaggio è importante.
    <button type="button" class="btn-close" data-bs-dismiss="alert"></button>
</div>
```

## 🏷️ Badge - Etichette

```html
<h1>Notifiche <span class="badge bg-danger">5</span></h1>

<button class="btn btn-primary">
    Messaggi <span class="badge bg-light text-dark">12</span>
</button>

<span class="badge bg-primary">Nuovo</span>
<span class="badge bg-success">Attivo</span>
<span class="badge bg-danger">Urgente</span>
```

## 🪟 Modal - Finestre Popup

```html
<!-- Pulsante che apre il modal -->
<button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#myModal">
    Apri Modal
</button>

<!-- Il Modal -->
<div class="modal fade" id="myModal" tabindex="-1">
    <div class="modal-dialog">
        <div class="modal-content">
            <div class="modal-header">
                <h5 class="modal-title">Titolo Modal</h5>
                <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
            </div>
            <div class="modal-body">
                <p>Contenuto del modal qui...</p>
            </div>
            <div class="modal-footer">
                <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Chiudi</button>
                <button type="button" class="btn btn-primary">Salva</button>
            </div>
        </div>
    </div>
</div>
```

## 🎨 Esempio Completo Harry Potter

```html
<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hogwarts - Home</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>

    <!-- Navbar -->
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
        <div class="container">
            <a class="navbar-brand" href="#">🏰 Hogwarts</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item">
                        <a class="nav-link active" href="#">Home</a>
                    </li>
                    <li class="nav-item dropdown">
                        <a class="nav-link dropdown-toggle" href="#" data-bs-toggle="dropdown">
                            Le Case
                        </a>
                        <ul class="dropdown-menu">
                            <li><a class="dropdown-item" href="#">Grifondoro</a></li>
                            <li><a class="dropdown-item" href="#">Serpeverde</a></li>
                            <li><a class="dropdown-item" href="#">Tassorosso</a></li>
                            <li><a class="dropdown-item" href="#">Corvonero</a></li>
                        </ul>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Materie</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Iscrizione</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <div class="bg-primary text-white text-center p-5">
        <h1>Benvenuto a Hogwarts</h1>
        <p class="lead">La scuola di magia più prestigiosa del mondo</p>
        <button class="btn btn-light btn-lg" data-bs-toggle="modal" data-bs-target="#iscrizioneModal">
            📜 Iscriviti Ora
        </button>
    </div>

    <div class="container my-5">

        <!-- Alert -->
        <div class="alert alert-warning alert-dismissible fade show">
            <strong>Nuove ammissioni!</strong> Sono aperte le iscrizioni per l'anno scolastico 2024/2025.
            <button type="button" class="btn-close" data-bs-dismiss="alert"></button>
        </div>

        <!-- Cards delle Case -->
        <h2 class="text-center mb-4">Le Nostre Case</h2>

        <div class="row">
            <!-- Grifondoro -->
            <div class="col-12 col-md-6 col-lg-3 mb-4">
                <div class="card h-100">
                    <div class="card-header bg-danger text-white text-center">
                        <h4>🦁 Grifondoro</h4>
                    </div>
                    <div class="card-body">
                        <p class="card-text">
                            <strong>Fondatore:</strong> Godric Grifondoro<br>
                            <strong>Valori:</strong> Coraggio, audacia<br>
                            <strong>Elemento:</strong> Fuoco
                        </p>
                        <span class="badge bg-danger">150 Studenti</span>
                    </div>
                    <div class="card-footer">
                        <button class="btn btn-danger btn-sm w-100">Scopri di più</button>
                    </div>
                </div>
            </div>

            <!-- Serpeverde -->
            <div class="col-12 col-md-6 col-lg-3 mb-4">
                <div class="card h-100">
                    <div class="card-header bg-success text-white text-center">
                        <h4>🐍 Serpeverde</h4>
                    </div>
                    <div class="card-body">
                        <p class="card-text">
                            <strong>Fondatore:</strong> Salazar Serpeverde<br>
                            <strong>Valori:</strong> Astuzia, ambizione<br>
                            <strong>Elemento:</strong> Acqua
                        </p>
                        <span class="badge bg-success">120 Studenti</span>
                    </div>
                    <div class="card-footer">
                        <button class="btn btn-success btn-sm w-100">Scopri di più</button>
                    </div>
                </div>
            </div>

            <!-- Tassorosso -->
            <div class="col-12 col-md-6 col-lg-3 mb-4">
                <div class="card h-100">
                    <div class="card-header bg-warning text-center">
                        <h4>🦡 Tassorosso</h4>
                    </div>
                    <div class="card-body">
                        <p class="card-text">
                            <strong>Fondatore:</strong> Tosca Tassorosso<br>
                            <strong>Valori:</strong> Lealtà, pazienza<br>
                            <strong>Elemento:</strong> Terra
                        </p>
                        <span class="badge bg-warning text-dark">135 Studenti</span>
                    </div>
                    <div class="card-footer">
                        <button class="btn btn-warning btn-sm w-100">Scopri di più</button>
                    </div>
                </div>
            </div>

            <!-- Corvonero -->
            <div class="col-12 col-md-6 col-lg-3 mb-4">
                <div class="card h-100">
                    <div class="card-header bg-primary text-white text-center">
                        <h4>🦅 Corvonero</h4>
                    </div>
                    <div class="card-body">
                        <p class="card-text">
                            <strong>Fondatore:</strong> Corinna Corvonero<br>
                            <strong>Valori:</strong> Intelligenza, creatività<br>
                            <strong>Elemento:</strong> Aria
                        </p>
                        <span class="badge bg-primary">110 Studenti</span>
                    </div>
                    <div class="card-footer">
                        <button class="btn btn-primary btn-sm w-100">Scopri di più</button>
                    </div>
                </div>
            </div>
        </div>

        <!-- Sezione Info -->
        <div class="row mt-5">
            <div class="col-lg-6 mb-3">
                <div class="alert alert-success">
                    <h5>✅ Anno Scolastico</h5>
                    <p class="mb-0">Le lezioni iniziano il 1° Settembre e terminano a Giugno.</p>
                </div>
            </div>
            <div class="col-lg-6 mb-3">
                <div class="alert alert-info">
                    <h5>📚 Materie</h5>
                    <p class="mb-0">Pozioni, Incantesimi, Trasfigurazione, Difesa e molto altro!</p>
                </div>
            </div>
        </div>

    </div>

    <!-- Modal Iscrizione -->
    <div class="modal fade" id="iscrizioneModal" tabindex="-1">
        <div class="modal-dialog">
            <div class="modal-content">
                <div class="modal-header bg-primary text-white">
                    <h5 class="modal-title">Iscrizione a Hogwarts</h5>
                    <button type="button" class="btn-close btn-close-white" data-bs-dismiss="modal"></button>
                </div>
                <div class="modal-body">
                    <form>
                        <div class="mb-3">
                            <label for="nome" class="form-label">Nome Completo</label>
                            <input type="text" class="form-control" id="nome" required>
                        </div>
                        <div class="mb-3">
                            <label for="email" class="form-label">Email</label>
                            <input type="email" class="form-control" id="email" required>
                        </div>
                        <div class="mb-3">
                            <label for="casa" class="form-label">Casa Preferita</label>
                            <select class="form-select" id="casa">
                                <option>Grifondoro</option>
                                <option>Serpeverde</option>
                                <option>Tassorosso</option>
                                <option>Corvonero</option>
                            </select>
                        </div>
                    </form>
                </div>
                <div class="modal-footer">
                    <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Chiudi</button>
                    <button type="button" class="btn btn-primary">Invia Candidatura</button>
                </div>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <div class="bg-dark text-white text-center p-4">
        <p class="mb-0">&copy; 2024 Hogwarts School</p>
        <small>Draco Dormiens Nunquam Titillandus</small>
    </div>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

## 🏆 Challenge: Pagina Materie

Crea `materie.html` con componenti Bootstrap!

**Requisiti:**
1. Navbar con menu "Home", "Case", "Materie", "Professori"
2. Hero section con titolo e pulsante
3. 6 card (2 righe da 3) per le materie:
   - Pozioni, Incantesimi, Trasfigurazione
   - Difesa, Erbologia, Volo
4. Ogni card con header colorato, body, badge (numero studenti), footer con pulsante
5. Un alert di avviso
6. Un modal "Info Materia" che si apre cliccando un pulsante
7. Footer scuro

<details>
<summary>💡 Soluzione Challenge</summary>

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

    <!-- Navbar -->
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
        <div class="container">
            <a class="navbar-brand" href="#">🏰 Hogwarts</a>
            <div class="collapse navbar-collapse">
                <ul class="navbar-nav">
                    <li class="nav-item"><a class="nav-link" href="#">Home</a></li>
                    <li class="nav-item"><a class="nav-link" href="#">Case</a></li>
                    <li class="nav-item"><a class="nav-link active" href="#">Materie</a></li>
                    <li class="nav-item"><a class="nav-link" href="#">Professori</a></li>
                </ul>
            </div>
        </div>
    </nav>

    <!-- Hero -->
    <div class="bg-primary text-white text-center p-5">
        <h1>Le Nostre Materie</h1>
        <p class="lead">Scopri cosa studierai a Hogwarts</p>
        <button class="btn btn-light" data-bs-toggle="modal" data-bs-target="#infoModal">📖 Più Info</button>
    </div>

    <div class="container my-5">

        <div class="alert alert-info">
            <strong>Nota:</strong> Tutte le materie sono obbligatorie per i primi 5 anni.
        </div>

        <div class="row">
            <!-- Pozioni -->
            <div class="col-md-4 mb-4">
                <div class="card h-100">
                    <div class="card-header bg-success text-white"><h5>🧪 Pozioni</h5></div>
                    <div class="card-body">
                        <p>Impara a creare pozioni magiche.</p>
                        <span class="badge bg-success">150 studenti</span>
                    </div>
                    <div class="card-footer">
                        <button class="btn btn-success btn-sm">Dettagli</button>
                    </div>
                </div>
            </div>

            <!-- Incantesimi -->
            <div class="col-md-4 mb-4">
                <div class="card h-100">
                    <div class="card-header bg-primary text-white"><h5>✨ Incantesimi</h5></div>
                    <div class="card-body">
                        <p>Studia incantesimi e magie.</p>
                        <span class="badge bg-primary">200 studenti</span>
                    </div>
                    <div class="card-footer">
                        <button class="btn btn-primary btn-sm">Dettagli</button>
                    </div>
                </div>
            </div>

            <!-- Trasfigurazione -->
            <div class="col-md-4 mb-4">
                <div class="card h-100">
                    <div class="card-header bg-warning"><h5>🐈 Trasfigurazione</h5></div>
                    <div class="card-body">
                        <p>Trasforma oggetti e animali.</p>
                        <span class="badge bg-warning text-dark">180 studenti</span>
                    </div>
                    <div class="card-footer">
                        <button class="btn btn-warning btn-sm">Dettagli</button>
                    </div>
                </div>
            </div>

            <!-- Altre 3 materie simili... -->
        </div>
    </div>

    <!-- Modal -->
    <div class="modal fade" id="infoModal">
        <div class="modal-dialog">
            <div class="modal-content">
                <div class="modal-header">
                    <h5>Info Materie</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
                </div>
                <div class="modal-body">
                    <p>Le materie sono obbligatorie fino al quinto anno.</p>
                </div>
            </div>
        </div>
    </div>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```
</details>

## ✅ Checklist

- [ ] So creare card con header, body, footer
- [ ] So costruire una navbar responsive
- [ ] So usare alert e badge
- [ ] So implementare modal
- [ ] Ho completato il challenge Materie

## 🎯 Prossimi Passi

Nella [prossima lezione](07-responsive-design.md) approfondiremo il **design responsive**!

---

*"La pratica rende perfetti!"* - Hermione 🎓
