# Esercizio 4: Layout delle Case con Bootstrap Grid

## 📖 Storia / Contesto

Il Professor Silente vuole rinnovare il Grande Salone di Hogwarts e ti ha chiesto di creare una pagina web che mostri le 4 case in modo ordinato e responsive. Usa il Grid System di Bootstrap per organizzare tutto!

## 🎯 Obiettivo

Imparare a usare il Grid System di Bootstrap per creare layout responsive che si adattano a mobile, tablet e desktop.

## 📋 Richieste

Crea `case-grid.html` con Bootstrap 5 che include:

1. **Bootstrap CDN** nel `<head>`
2. **Container** per centrare il contenuto
3. **Titolo** centrato: "Le Quattro Case di Hogwarts"

4. **Griglia delle Case**:
   - Mobile (xs): 1 casa per riga (100% larghezza)
   - Tablet (md): 2 case per riga (50% ciascuna)
   - Desktop (lg): 4 case per riga (25% ciascuna)

5. **Ogni casa deve avere**:
   - Box colorato (usa bg-danger, bg-success, bg-warning, bg-primary)
   - Nome della casa
   - Fondatore
   - Valori
   - Padding appropriato

6. **Sezione Info** con layout sidebar + content:
   - Mobile: entrambi full-width
   - Desktop: sidebar 25% (col-lg-3), content 75% (col-lg-9)

7. **Footer** centrato con sfondo scuro

## 🚀 Starter Code

```html
<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Le Case di Hogwarts</title>

    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>

    <div class="container my-5">
        <h1 class="text-center mb-5">Le Quattro Case di Hogwarts</h1>

        <!-- Grid delle Case -->
        <div class="row">
            <!-- Grifondoro -->
            <div class="col-12 col-md-6 col-lg-3 mb-4">
                <!-- Completa qui -->
            </div>

            <!-- Continua con altre case... -->
        </div>
    </div>

    <!-- Bootstrap JS -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

## ✅ Output Atteso

La pagina deve:
- Mostrare 4 case in grid responsive
- Su mobile: 1 colonna
- Su tablet: 2 colonne
- Su desktop: 4 colonne
- Colori diversi per ogni casa
- Layout sidebar + content nella sezione info
- Design pulito e professionale

## 💡 Suggerimenti

1. Usa `col-12 col-md-6 col-lg-3` per la griglia responsive
2. Usa classi Bootstrap per colori: `bg-danger`, `text-white`, ecc.
3. Usa `p-4` per padding interno
4. Usa `mb-4` per margine bottom tra le case
5. Usa `h-100` per altezze uguali
6. Testa ridimensionando la finestra del browser

## ✨ Soluzione Completa

<details>
<summary>💡 Clicca qui per vedere la soluzione</summary>

```html
<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Le Case di Hogwarts - Grid Layout</title>

    <!-- Bootstrap 5 CDN -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>

    <!-- Hero Section -->
    <div class="bg-dark text-white text-center p-5">
        <h1>Le Quattro Case di Hogwarts</h1>
        <p class="lead">Ogni casa rappresenta valori unici e importanti</p>
    </div>

    <!-- Container Principale -->
    <div class="container my-5">

        <!-- Grid delle 4 Case -->
        <div class="row g-4">

            <!-- Grifondoro -->
            <div class="col-12 col-md-6 col-lg-3">
                <div class="bg-danger text-white p-4 h-100 text-center">
                    <h2>🦁</h2>
                    <h3>Grifondoro</h3>
                    <hr class="bg-white">
                    <p><strong>Fondatore:</strong><br>Godric Grifondoro</p>
                    <p><strong>Valori:</strong><br>Coraggio e audacia</p>
                    <p><strong>Colori:</strong><br>Rosso e oro</p>
                </div>
            </div>

            <!-- Serpeverde -->
            <div class="col-12 col-md-6 col-lg-3">
                <div class="bg-success text-white p-4 h-100 text-center">
                    <h2>🐍</h2>
                    <h3>Serpeverde</h3>
                    <hr class="bg-white">
                    <p><strong>Fondatore:</strong><br>Salazar Serpeverde</p>
                    <p><strong>Valori:</strong><br>Astuzia e ambizione</p>
                    <p><strong>Colori:</strong><br>Verde e argento</p>
                </div>
            </div>

            <!-- Tassorosso -->
            <div class="col-12 col-md-6 col-lg-3">
                <div class="bg-warning p-4 h-100 text-center">
                    <h2>🦡</h2>
                    <h3>Tassorosso</h3>
                    <hr>
                    <p><strong>Fondatore:</strong><br>Tosca Tassorosso</p>
                    <p><strong>Valori:</strong><br>Lealtà e pazienza</p>
                    <p><strong>Colori:</strong><br>Giallo e nero</p>
                </div>
            </div>

            <!-- Corvonero -->
            <div class="col-12 col-md-6 col-lg-3">
                <div class="bg-primary text-white p-4 h-100 text-center">
                    <h2>🦅</h2>
                    <h3>Corvonero</h3>
                    <hr class="bg-white">
                    <p><strong>Fondatore:</strong><br>Corinna Corvonero</p>
                    <p><strong>Valori:</strong><br>Intelligenza e creatività</p>
                    <p><strong>Colori:</strong><br>Blu e bronzo</p>
                </div>
            </div>

        </div>

        <hr class="my-5">

        <!-- Layout Sidebar + Content -->
        <div class="row">

            <!-- Sidebar (25% su desktop, 100% su mobile) -->
            <div class="col-12 col-lg-3 mb-4 mb-lg-0">
                <div class="bg-light p-3">
                    <h4>Menu</h4>
                    <ul class="list-unstyled">
                        <li><a href="#" class="text-decoration-none">Storia delle Case</a></li>
                        <li><a href="#" class="text-decoration-none">Dormitori</a></li>
                        <li><a href="#" class="text-decoration-none">Sale Comuni</a></li>
                        <li><a href="#" class="text-decoration-none">Fantasmi</a></li>
                        <li><a href="#" class="text-decoration-none">Coppa delle Case</a></li>
                    </ul>
                </div>
            </div>

            <!-- Content (75% su desktop, 100% su mobile) -->
            <div class="col-12 col-lg-9">
                <h2>Storia delle Case</h2>
                <p>
                    Le quattro case di Hogwarts furono fondate oltre mille anni fa
                    dai quattro maghi più potenti dell'epoca. Ogni casa porta il nome
                    del suo fondatore e riflette i valori che lui o lei considerava
                    più importanti.
                </p>

                <h3 class="mt-4">Il Cappello Parlante</h3>
                <p>
                    Ogni nuovo studente viene smistato in una delle quattro case
                    dal Cappello Parlante, che valuta le qualità personali e le
                    preferenze dello studente.
                </p>

                <!-- Sottogrid: 2 colonne -->
                <div class="row mt-4">
                    <div class="col-12 col-md-6 mb-3">
                        <div class="border p-3">
                            <h5>📍 Sala Comune</h5>
                            <p>Ogni casa ha la propria sala comune dove gli studenti
                            si riuniscono e socializzano.</p>
                        </div>
                    </div>
                    <div class="col-12 col-md-6 mb-3">
                        <div class="border p-3">
                            <h5>🏆 Punti Casa</h5>
                            <p>Gli studenti guadagnano o perdono punti per la loro
                            casa durante l'anno scolastico.</p>
                        </div>
                    </div>
                </div>
            </div>

        </div>

    </div>

    <!-- Footer -->
    <div class="bg-dark text-white text-center p-4 mt-5">
        <p class="mb-0">&copy; 2024 Hogwarts School</p>
        <small>Draco Dormiens Nunquam Titillandus</small>
    </div>

    <!-- Bootstrap JS -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```
</details>

## 🎨 Varianti e Sfide Bonus

### Variante 1: Aggiungi Studenti Famosi
Sotto ogni casa, aggiungi una lista di 3 studenti famosi in una sotto-griglia

### Variante 2: Card Bootstrap
Trasforma i box delle case in `<div class="card">` con header, body e footer

### Variante 3: Breakpoint XXL
Aggiungi un breakpoint per schermi molto grandi (XXL) dove mostri anche altre informazioni

### Variante 4: Offset
Crea una sezione con una card centrata usando `offset`

## 🔍 Checklist di Verifica

- [ ] Bootstrap CDN incluso correttamente
- [ ] Usato `container` per centrare il contenuto
- [ ] Grid con `row` e `col-*`
- [ ] Responsive: 1 col mobile, 2 tablet, 4 desktop
- [ ] Tutte le 4 case presenti con colori diversi
- [ ] Layout sidebar + content funzionante
- [ ] Altezze uguali con `h-100`
- [ ] Testato su diversi schermi (F12 > Device Toolbar)

## 📚 Cosa Hai Imparato

- Sistema a 12 colonne di Bootstrap
- Classi responsive (`col-12`, `col-md-6`, `col-lg-3`)
- Container e row
- Gutters (spazi tra colonne)
- Layout sidebar + content
- Classi utility (bg, text, p, m, h-100)
- Come testare il responsive

## 🎯 Prossimo Passo

Ottimo lavoro! Passa al [Esercizio 5: Navbar](es05-navbar.md) per creare un menu di navigazione professionale!

---

*"L'organizzazione è la chiave della magia, così come il Grid è la chiave del layout!"* 🎯✨
