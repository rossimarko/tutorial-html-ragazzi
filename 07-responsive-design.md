# Lezione 7: Responsive Design - Siti per Tutti i Dispositivi

Benvenuto alla settima lezione! Oggi approfondirai il design responsive: come creare siti che funzionano perfettamente su telefono, tablet e computer!

## 🎯 Obiettivi della Lezione

Alla fine di questa lezione saprai:
- Cos'è il design responsive e perché è importante
- Usare i breakpoint di Bootstrap efficacemente
- Nascondere/mostrare elementi su dispositivi diversi
- Creare layout che si adattano automaticamente
- Testare il tuo sito su schermi diversi

## 🧙 Concetti Fondamentali

### Cos'è il Responsive Design?

**Responsive** significa che il tuo sito **si adatta** alla dimensione dello schermo:
- Su **telefono** → 1 colonna, menu hamburger, testo grande
- Su **tablet** → 2 colonne, layout intermedio
- Su **computer** → 3-4 colonne, layout complesso

Il tuo sito "risponde" (respond) alla dimensione dello schermo!

### Perché è Importante?

Guarda queste statistiche:
- 📱 60% delle persone naviga da telefono
- 💻 30% da computer
- 📱 10% da tablet

Se il tuo sito non funziona su telefono, perdi la maggior parte dei visitatori!

## ⚡ Analogia Harry Potter

Il design responsive è come **l'Incantesimo Adattamento**:

- Il **Castello di Hogwarts** si adatta: le scale si muovono, le porte cambiano posto
- Il tuo **sito responsive** si adatta: colonne diventano righe, menu si nasconde, immagini si ridimensionano

Pensa alla **Tenda di Mr. Weasley**: piccola fuori, enorme dentro! Il responsive fa lo stesso: usa bene lo spazio disponibile.

## 💻 Breakpoint Bootstrap

Bootstrap divide gli schermi in 5 categorie:

| Breakpoint | Dimensione | Dispositivo | Classe |
|-----------|------------|-------------|--------|
| **xs** | < 576px | Telefono piccolo | `col-*` |
| **sm** | ≥ 576px | Telefono grande | `col-sm-*` |
| **md** | ≥ 768px | Tablet | `col-md-*` |
| **lg** | ≥ 992px | Desktop | `col-lg-*` |
| **xl** | ≥ 1200px | Desktop grande | `col-xl-*` |
| **xxl** | ≥ 1400px | Desktop enorme | `col-xxl-*` |

### Come Funzionano

Quando scrivi:
```html
<div class="col-12 col-md-6 col-lg-4">
```

Significa:
- **Mobile (xs)**: occupa 12/12 (100% - tutto lo schermo)
- **Tablet (md)**: occupa 6/12 (50% - metà schermo)
- **Desktop (lg)**: occupa 4/12 (33% - un terzo)

## 📱 Mobile First

La filosofia di Bootstrap è **Mobile First**: parti dal telefono, poi aggiungi per schermi più grandi.

```html
<!-- ✅ GIUSTO: Mobile First -->
<div class="col-12 col-md-6 col-lg-4">
    <!--
    Mobile: 12 (full width)
    Tablet: 6 (metà)
    Desktop: 4 (un terzo)
    -->
</div>

<!-- ❌ SBAGLIATO: Non serve specificare tutto -->
<div class="col-xs-12 col-sm-12 col-md-6 col-lg-4">
    <!-- Troppo complicato -->
</div>
```

## 🎨 Esempio Responsive Completo

```html
<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hogwarts Responsive</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>

    <!-- Navbar Responsive -->
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
        <div class="container">
            <a class="navbar-brand" href="#">🏰 Hogwarts</a>
            <!-- Pulsante hamburger (visibile solo su mobile) -->
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <!-- Menu (collassa su mobile) -->
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item"><a class="nav-link" href="#">Home</a></li>
                    <li class="nav-item"><a class="nav-link" href="#">Case</a></li>
                    <li class="nav-item"><a class="nav-link" href="#">Materie</a></li>
                </ul>
            </div>
        </div>
    </nav>

    <!-- Hero Section - Padding responsivo -->
    <div class="bg-primary text-white text-center p-3 p-md-5">
        <h1 class="display-6 display-md-4">Benvenuto a Hogwarts</h1>
        <p class="lead d-none d-md-block">La scuola di magia più famosa</p>
    </div>

    <div class="container my-4 my-md-5">

        <!-- Grid Responsive: 1 col mobile, 2 col tablet, 4 col desktop -->
        <h2 class="text-center mb-4">Le Quattro Case</h2>

        <div class="row g-3 g-md-4">

            <div class="col-12 col-sm-6 col-lg-3">
                <div class="card bg-danger text-white h-100">
                    <div class="card-body text-center">
                        <h3>🦁</h3>
                        <h5>Grifondoro</h5>
                        <p class="d-none d-lg-block">Coraggio e audacia</p>
                    </div>
                </div>
            </div>

            <div class="col-12 col-sm-6 col-lg-3">
                <div class="card bg-success text-white h-100">
                    <div class="card-body text-center">
                        <h3>🐍</h3>
                        <h5>Serpeverde</h5>
                        <p class="d-none d-lg-block">Astuzia e ambizione</p>
                    </div>
                </div>
            </div>

            <div class="col-12 col-sm-6 col-lg-3">
                <div class="card bg-warning h-100">
                    <div class="card-body text-center">
                        <h3>🦡</h3>
                        <h5>Tassorosso</h5>
                        <p class="d-none d-lg-block">Lealtà e pazienza</p>
                    </div>
                </div>
            </div>

            <div class="col-12 col-sm-6 col-lg-3">
                <div class="card bg-primary text-white h-100">
                    <div class="card-body text-center">
                        <h3>🦅</h3>
                        <h5>Corvonero</h5>
                        <p class="d-none d-lg-block">Intelligenza e creatività</p>
                    </div>
                </div>
            </div>

        </div>

        <hr class="my-5">

        <!-- Layout Sidebar: Full width mobile, sidebar+content desktop -->
        <div class="row">

            <!-- Sidebar: Full su mobile, 1/4 su desktop -->
            <div class="col-12 col-lg-3 mb-4 mb-lg-0">
                <div class="bg-light p-3">
                    <h4 class="h5 h-lg-4">Menu</h4>
                    <ul class="list-unstyled">
                        <li><a href="#">Storia</a></li>
                        <li><a href="#">Professori</a></li>
                        <li><a href="#">Materie</a></li>
                        <li class="d-none d-lg-block"><a href="#">Biblioteca</a></li>
                        <li class="d-none d-lg-block"><a href="#">Sala Grande</a></li>
                    </ul>
                </div>
            </div>

            <!-- Contenuto: Full su mobile, 3/4 su desktop -->
            <div class="col-12 col-lg-9">
                <h2 class="h3 h-md-2">Storia di Hogwarts</h2>
                <p>
                    Hogwarts fu fondata oltre mille anni fa. Il castello ospita
                    centinaia di studenti ogni anno.
                </p>

                <!-- Bottoni responsive -->
                <button class="btn btn-primary btn-sm btn-md-lg w-100 w-md-auto">
                    📖 Leggi di più
                </button>
            </div>

        </div>

    </div>

    <!-- Footer con padding responsive -->
    <div class="bg-dark text-white text-center p-3 p-md-4 mt-5">
        <p class="mb-0">© 2024 Hogwarts</p>
        <small class="d-none d-md-inline">Draco Dormiens Nunquam Titillandus</small>
    </div>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

## 👁️ Mostrare/Nascondere Elementi

Bootstrap ha classi per mostrare o nascondere elementi su schermi specifici.

### Display Utilities

```html
<!-- Nascosto su mobile, visibile da tablet in su -->
<div class="d-none d-md-block">
    Visibile solo su tablet e desktop
</div>

<!-- Visibile solo su mobile -->
<div class="d-block d-md-none">
    Visibile solo su telefono
</div>

<!-- Visibile solo su desktop -->
<div class="d-none d-lg-block">
    Visibile solo su desktop
</div>
```

### Esempi Pratici

```html
<!-- Testo lungo solo su desktop -->
<p class="d-none d-lg-block">
    Questo paragrafo lungo è visibile solo su desktop perché
    su mobile occuperebbe troppo spazio.
</p>

<!-- Immagine piccola su mobile, grande su desktop -->
<img src="logo.png" class="d-md-none" width="50">
<img src="logo.png" class="d-none d-md-block" width="200">

<!-- Menu completo su desktop, mini su mobile -->
<nav class="d-none d-lg-block">Menu completo</nav>
<nav class="d-lg-none">Menu mini</nav>
```

## 📐 Classi Responsive Varie

### Spaziature Responsive

```html
<!-- Padding piccolo su mobile, grande su desktop -->
<div class="p-2 p-md-4 p-lg-5">
    Padding responsive
</div>

<!-- Margin bottom diverso -->
<div class="mb-3 mb-md-5">
    Margin responsive
</div>
```

### Testo Responsive

```html
<!-- Dimensione testo responsive -->
<h1 class="display-6 display-md-4 display-lg-3">
    Titolo che cresce su schermi grandi
</h1>

<!-- Allineamento responsive -->
<p class="text-center text-md-start">
    Centrato su mobile, sinistra su desktop
</p>
```

### Bottoni Responsive

```html
<!-- Bottone che diventa più grande su desktop -->
<button class="btn btn-primary btn-sm btn-lg-lg">
    Bottone responsive
</button>

<!-- Bottone full-width su mobile, auto su desktop -->
<button class="btn btn-success w-100 w-md-auto">
    Invia
</button>
```

## 🧪 Testare il Responsive

### Nel Browser

1. Apri il tuo sito
2. Premi `F12` (o `Ctrl+Shift+I`)
3. Clicca l'icona "Device Toolbar" (📱)
4. Scegli un dispositivo o ridimensiona manualmente

### Shortcut Browser

- **Chrome/Edge**: `Ctrl+Shift+M` (Windows) / `Cmd+Shift+M` (Mac)
- **Firefox**: `Ctrl+Shift+M` (Windows) / `Cmd+Option+M` (Mac)

### Testare su Telefono Vero

1. Assicurati che PC e telefono siano sulla stessa WiFi
2. Trova l'IP del tuo PC (es: 192.168.1.100)
3. Avvia Live Server
4. Sul telefono vai a `http://192.168.1.100:5500`

## 🏆 Challenge: Portfolio Responsive

Crea `portfolio.html` - una pagina responsive completa!

**Requisiti:**
1. Navbar che collassa su mobile
2. Hero section con padding responsive (`p-3 p-md-5`)
3. Griglia progetti:
   - 1 colonna su mobile
   - 2 colonne su tablet (`col-md-6`)
   - 3 colonne su desktop (`col-lg-4`)
4. Sidebar che va full-width su mobile
5. Elementi nascosti su mobile con `d-none d-md-block`
6. Bottone full-width su mobile, auto su desktop
7. Footer con testo nascosto su mobile

<details>
<summary>💡 Soluzione</summary>

```html
<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio Magico</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>

    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
        <div class="container">
            <a class="navbar-brand" href="#">🪄 Il Mio Portfolio</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#nav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="nav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item"><a class="nav-link" href="#">Home</a></li>
                    <li class="nav-item"><a class="nav-link" href="#">Progetti</a></li>
                    <li class="nav-item"><a class="nav-link" href="#">Contatti</a></li>
                </ul>
            </div>
        </div>
    </nav>

    <div class="bg-primary text-white text-center p-3 p-md-5">
        <h1 class="display-5 display-md-3">I Miei Progetti Magici</h1>
        <p class="lead d-none d-md-block">Scopri cosa ho creato!</p>
    </div>

    <div class="container my-4 my-md-5">

        <div class="row">
            <div class="col-12 col-lg-3 mb-4">
                <div class="bg-light p-3">
                    <h4>Categorie</h4>
                    <ul class="list-unstyled">
                        <li>Pozioni</li>
                        <li>Incantesimi</li>
                        <li class="d-none d-lg-block">Trasfigurazioni</li>
                    </ul>
                </div>
            </div>

            <div class="col-12 col-lg-9">
                <div class="row g-3 g-md-4">
                    <div class="col-12 col-md-6 col-lg-4">
                        <div class="card">
                            <div class="card-body">
                                <h5>Progetto 1</h5>
                                <p class="d-none d-md-block">Descrizione progetto</p>
                            </div>
                        </div>
                    </div>
                    <div class="col-12 col-md-6 col-lg-4">
                        <div class="card">
                            <div class="card-body">
                                <h5>Progetto 2</h5>
                                <p class="d-none d-md-block">Descrizione progetto</p>
                            </div>
                        </div>
                    </div>
                    <div class="col-12 col-md-6 col-lg-4">
                        <div class="card">
                            <div class="card-body">
                                <h5>Progetto 3</h5>
                                <p class="d-none d-md-block">Descrizione progetto</p>
                            </div>
                        </div>
                    </div>
                </div>

                <button class="btn btn-primary mt-4 w-100 w-md-auto">
                    Vedi Tutti
                </button>
            </div>
        </div>

    </div>

    <div class="bg-dark text-white text-center p-3 p-md-4">
        <p class="mb-0">© 2024 Portfolio</p>
        <small class="d-none d-md-inline">Creato con magia e Bootstrap</small>
    </div>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```
</details>

## 💡 Best Practices

### 1. Meta Viewport (Obbligatorio!)

Sempre includere nel `<head>`:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

Senza questo, il responsive NON funziona su mobile!

### 2. Testa su Dispositivi Reali

Non basta il browser. Testa su:
- Telefono vero
- Tablet se hai
- Diversi browser

### 3. Immagini Responsive

```html
<!-- Immagini che si adattano -->
<img src="foto.jpg" class="img-fluid" alt="Descrizione">
```

### 4. Non Esagerare

Non nascondere troppo contenuto su mobile. L'utente su telefono deve vedere l'essenziale!

## ✅ Checklist

- [ ] Capisco i breakpoint (sm, md, lg, xl)
- [ ] So creare griglie responsive
- [ ] So nascondere/mostrare elementi con `d-none` e `d-*-block`
- [ ] So usare spaziature responsive
- [ ] So testare il sito su diversi schermi
- [ ] Ho completato il challenge Portfolio

## 🎯 Prossimi Passi

Fantastico! Ora sai creare siti responsive!

Nella [prossima lezione](08-progetto-finale.md) metteremo insieme **tutto quello che hai imparato** per creare il **Sito Hogwarts completo**!

---

*"L'adattabilità è la vera magia!"* 🪄✨
