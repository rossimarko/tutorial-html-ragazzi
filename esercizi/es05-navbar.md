# Esercizio 5: Navbar Professionale per Hogwarts

## 📖 Storia / Contesto

Il sito di Hogwarts ha bisogno di un menu di navigazione professionale! Il Professor Silente ti ha incaricato di creare una navbar che funzioni perfettamente su tutti i dispositivi: desktop, tablet e telefono. Deve essere elegante come la scuola stessa!

## 🎯 Obiettivo

Creare una navbar completa con Bootstrap che include logo, menu, dropdown e che si adatta perfettamente a mobile (hamburger menu).

## 📋 Richieste

Crea `navbar-hogwarts.html` con:

1. **Navbar Bootstrap** scura (`navbar-dark bg-dark`)
2. **Brand/Logo**: "🏰 Hogwarts"
3. **Pulsante Hamburger** per mobile (toggler)
4. **Menu items**:
   - Home (link attivo)
   - Le Case
   - Materie
   - Iscrizione

5. **Dropdown Menu** "Le Case" con:
   - Grifondoro
   - Serpeverde
   - Tassorosso
   - Corvonero

6. **Contenuto sotto la navbar**:
   - Hero section
   - Paragrafo di benvenuto

7. **Responsive**:
   - Su desktop: menu orizzontale
   - Su mobile: menu hamburger collapse

## 🚀 Starter Code

```html
<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Navbar Hogwarts</title>

    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>

    <!-- Navbar -->
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
        <div class="container">
            <a class="navbar-brand" href="#">🏰 Hogwarts</a>

            <!-- Pulsante hamburger -->
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>

            <!-- Menu -->
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <!-- Completa tu... -->
                </ul>
            </div>
        </div>
    </nav>

    <!-- Contenuto -->

    <!-- Bootstrap JS -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

## ✅ Output Atteso

La navbar deve:
- Essere fissa in alto con sfondo scuro
- Mostrare logo "Hogwarts" a sinistra
- Mostrare menu a destra
- Avere link "Home" attivo (evidenziato)
- Avere dropdown "Le Case" funzionante
- Su mobile: collassare in menu hamburger
- Essere responsive e professionale

## 💡 Suggerimenti

1. Usa `navbar-expand-lg` per espandere su schermi grandi
2. `ms-auto` sposta il menu a destra
3. Classe `active` evidenzia il link corrente
4. Per dropdown serve `dropdown-toggle` e `dropdown-menu`
5. **IMPORTANTE**: Serve Bootstrap JS per hamburger e dropdown!
6. Testa su mobile con F12 > Device Toolbar

## ✨ Soluzione Completa

<details>
<summary>💡 Clicca qui per vedere la soluzione</summary>

```html
<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hogwarts - Navbar Completa</title>

    <!-- Bootstrap 5 CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>

    <!-- Navbar -->
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark sticky-top">
        <div class="container">

            <!-- Brand / Logo -->
            <a class="navbar-brand" href="index.html">
                🏰 <strong>Hogwarts</strong>
            </a>

            <!-- Hamburger Button (visibile solo su mobile) -->
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>

            <!-- Menu (collassa su mobile) -->
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">

                    <!-- Home -->
                    <li class="nav-item">
                        <a class="nav-link active" href="index.html">Home</a>
                    </li>

                    <!-- Dropdown: Le Case -->
                    <li class="nav-item dropdown">
                        <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown">
                            Le Case
                        </a>
                        <ul class="dropdown-menu">
                            <li><a class="dropdown-item" href="grifondoro.html">🦁 Grifondoro</a></li>
                            <li><a class="dropdown-item" href="serpeverde.html">🐍 Serpeverde</a></li>
                            <li><a class="dropdown-item" href="tassorosso.html">🦡 Tassorosso</a></li>
                            <li><a class="dropdown-item" href="corvonero.html">🦅 Corvonero</a></li>
                        </ul>
                    </li>

                    <!-- Materie -->
                    <li class="nav-item">
                        <a class="nav-link" href="materie.html">Materie</a>
                    </li>

                    <!-- Iscrizione -->
                    <li class="nav-item">
                        <a class="nav-link" href="iscrizione.html">Iscrizione</a>
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

    <!-- Contenuto Principale -->
    <div class="container my-5">
        <div class="row">
            <div class="col-lg-8 mx-auto">
                <h2>Chi Siamo</h2>
                <p>
                    Hogwarts è stata fondata oltre mille anni fa da quattro grandi maghi:
                    Godric Grifondoro, Salazar Serpeverde, Tosca Tassorosso e Corinna Corvonero.
                </p>
                <p>
                    Ogni anno, centinaia di giovani maghi e streghe vengono ammessi per
                    imparare le arti magiche più avanzate sotto la guida dei migliori
                    professori del mondo magico.
                </p>

                <h3 class="mt-4">Cosa Offriamo</h3>
                <ul>
                    <li>Insegnamento di qualità da professori esperti</li>
                    <li>Castello storico con sale comuni accoglienti</li>
                    <li>Biblioteca con migliaia di libri magici</li>
                    <li>Campo di Quidditch professionale</li>
                    <li>Foresta didattica per Erbologia</li>
                </ul>

                <div class="alert alert-warning mt-4">
                    <strong>Nuove ammissioni!</strong> Le iscrizioni per l'anno 2024/2025
                    sono aperte. Affrettati a inviare la tua candidatura!
                </div>

                <div class="text-center mt-4">
                    <a href="iscrizione.html" class="btn btn-primary btn-lg">
                        Iscriviti Ora
                    </a>
                </div>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <div class="bg-dark text-white text-center p-4">
        <p class="mb-0">&copy; 2024 Hogwarts School of Witchcraft and Wizardry</p>
        <small class="text-muted">Draco Dormiens Nunquam Titillandus</small>
    </div>

    <!-- Bootstrap JS (OBBLIGATORIO per hamburger e dropdown!) -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```
</details>

## 🎨 Varianti e Sfide Bonus

### Variante 1: Navbar Sticky
Rendi la navbar fissa in alto quando scrolli con `sticky-top`:
```html
<nav class="navbar navbar-dark bg-dark sticky-top">
```

### Variante 2: Search Bar
Aggiungi una barra di ricerca nella navbar:
```html
<form class="d-flex ms-3">
    <input class="form-control me-2" type="search" placeholder="Cerca...">
    <button class="btn btn-outline-light" type="submit">Cerca</button>
</form>
```

### Variante 3: Navbar Chiara
Prova una navbar chiara invece che scura:
```html
<nav class="navbar navbar-expand-lg navbar-light bg-light">
```

### Variante 4: Multi-Dropdown
Aggiungi un secondo dropdown per "Materie" con sottovoci

## 🔍 Checklist di Verifica

- [ ] Bootstrap CSS e JS inclusi
- [ ] Navbar con `navbar`, `navbar-expand-lg`, `navbar-dark`, `bg-dark`
- [ ] Logo/Brand presente
- [ ] Pulsante hamburger (`navbar-toggler`)
- [ ] Menu con `collapse navbar-collapse`
- [ ] Link "Home" con classe `active`
- [ ] Dropdown "Le Case" funzionante
- [ ] Menu si allinea a destra con `ms-auto`
- [ ] Su mobile il menu si nasconde e appare con hamburger
- [ ] Dropdown si apre correttamente (click)
- [ ] Tutti i link hanno href (anche se finti)

## 📚 Cosa Hai Imparato

- Struttura navbar Bootstrap
- Brand e toggler
- Collapse per menu responsive
- Dropdown menu
- Classi navbar-expand-*
- Importanza di Bootstrap JS
- Hamburger menu per mobile
- Allineamento con ms-auto

## 🎯 Prossimo Passo

Eccellente! Hai completato tutti gli esercizi! 🎉

Ora sei pronto per il **[Progetto Finale](../progetti/progetto-finale.md)**: creare il sito completo di Hogwarts mettendo insieme tutto quello che hai imparato!

---

*"La navigazione è come la magia: deve essere intuitiva e funzionare sempre!"* 🧭✨
