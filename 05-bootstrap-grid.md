# Lezione 5: Bootstrap Grid System - Layout a Griglia

Benvenuto alla quinta lezione! Oggi imparerai il Grid System di Bootstrap: il sistema per organizzare il contenuto in righe e colonne. È la magia più potente di Bootstrap!

## 🎯 Obiettivi della Lezione

Alla fine di questa lezione saprai:
- Come funziona il sistema a 12 colonne
- Creare layout con righe (`row`) e colonne (`col`)
- Usare dimensioni responsive (col-md, col-lg, ecc.)
- Centrare e distribuire contenuti
- Creare layout complessi per il tuo sito

## 🧙 Concetti Fondamentali

### Cos'è il Grid System?

Il **Grid System** di Bootstrap è un sistema per **organizzare il contenuto** in righe e colonne, come una tabella invisibile.

Funziona così:
1. Crei una **riga** (`row`)
2. Dentro la riga crei **colonne** (`col`)
3. Ogni riga è divisa in **12 parti**
4. Tu decidi quanto spazio occupa ogni colonna

**Esempio:**
- 1 colonna che occupa tutto = `col-12`
- 2 colonne da metà schermo = `col-6` + `col-6`
- 3 colonne uguali = `col-4` + `col-4` + `col-4`

### Regola delle 12 Colonne

Ogni riga ha **12 unità** di spazio. Tu dividi queste 12 unità tra le tue colonne:

```
|  1  |  2  |  3  |  4  |  5  |  6  |  7  |  8  |  9  |  10 |  11 |  12 |
|--------------------------------- 12 unità ---------------------------------|
```

**Esempi di divisione:**
- `col-6` + `col-6` = 6 + 6 = 12 ✅
- `col-4` + `col-4` + `col-4` = 4 + 4 + 4 = 12 ✅
- `col-3` + `col-9` = 3 + 9 = 12 ✅
- `col-8` + `col-8` = 16 ❌ Va a capo!

## ⚡ Analogia Harry Potter

Pensa al Grid System come al **Grande Salone di Hogwarts**:

- La **row** (riga) = Un tavolo lungo del salone
- Le **col** (colonne) = I posti al tavolo
- Ogni tavolo ha **12 posti** (le 12 unità)
- Tu decidi quanti posti dare a ogni casa:
  - Grifondoro = 6 posti → `col-6`
  - Serpeverde = 4 posti → `col-4`
  - Altri = 2 posti → `col-2`
  - Totale = 12 ✅

Il Grid System ti permette di **organizzare gli studenti** (contenuti) ai tavoli (layout)!

## 💻 Sintassi Base

### Struttura Container > Row > Col

```html
<div class="container">
    <div class="row">
        <div class="col">
            Colonna 1
        </div>
        <div class="col">
            Colonna 2
        </div>
        <div class="col">
            Colonna 3
        </div>
    </div>
</div>
```

Questo crea **3 colonne uguali** (si dividono automaticamente).

### Colonne con Dimensioni Specifiche

```html
<div class="container">
    <div class="row">
        <div class="col-8">
            Larga (8 unità)
        </div>
        <div class="col-4">
            Stretta (4 unità)
        </div>
    </div>
</div>
```

### Layout Comuni

**2 colonne uguali (metà schermo ciascuna):**
```html
<div class="row">
    <div class="col-6">Prima metà</div>
    <div class="col-6">Seconda metà</div>
</div>
```

**3 colonne uguali (un terzo ciascuna):**
```html
<div class="row">
    <div class="col-4">Un terzo</div>
    <div class="col-4">Un terzo</div>
    <div class="col-4">Un terzo</div>
</div>
```

**Sidebar + Contenuto (25% + 75%):**
```html
<div class="row">
    <div class="col-3">Sidebar</div>
    <div class="col-9">Contenuto principale</div>
</div>
```

## 📱 Grid Responsive

Il vero potere del Grid è la **responsività**: layout diversi su schermi diversi!

### Breakpoints

Bootstrap ha 5 dimensioni schermo:
- **xs** (extra small) = Telefoni (< 576px) → `col-*`
- **sm** (small) = Telefoni grandi (≥ 576px) → `col-sm-*`
- **md** (medium) = Tablet (≥ 768px) → `col-md-*`
- **lg** (large) = Desktop (≥ 992px) → `col-lg-*`
- **xl** (extra large) = Desktop grandi (≥ 1200px) → `col-xl-*`

### Come Funziona

```html
<div class="col-12 col-md-6 col-lg-4">
    Contenuto
</div>
```

Significa:
- Su mobile (xs): occupa **12/12** (tutto lo schermo)
- Su tablet (md): occupa **6/12** (metà schermo)
- Su desktop (lg): occupa **4/12** (un terzo)

**Magico, vero?** Lo stesso codice si adatta automaticamente!

### Esempio Responsive

```html
<div class="container">
    <div class="row">
        <!-- Su mobile: 100%, su tablet: 50%, su desktop: 33% -->
        <div class="col-12 col-md-6 col-lg-4 bg-primary text-white p-3 mb-2">
            Box 1
        </div>
        <div class="col-12 col-md-6 col-lg-4 bg-success text-white p-3 mb-2">
            Box 2
        </div>
        <div class="col-12 col-md-6 col-lg-4 bg-danger text-white p-3 mb-2">
            Box 3
        </div>
    </div>
</div>
```

## 🎨 Esempio Harry Potter Completo

```html
<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Le Case di Hogwarts</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>

    <!-- Header -->
    <div class="bg-dark text-white text-center p-5">
        <h1>Le Quattro Case di Hogwarts</h1>
    </div>

    <div class="container my-5">

        <!-- 4 colonne uguali su desktop, 1 colonna su mobile -->
        <div class="row">

            <!-- Grifondoro -->
            <div class="col-12 col-md-6 col-lg-3 mb-4">
                <div class="bg-danger text-white p-4 h-100">
                    <h3>🦁 Grifondoro</h3>
                    <p><strong>Fondatore:</strong> Godric Grifondoro</p>
                    <p><strong>Valori:</strong> Coraggio, audacia</p>
                    <p><strong>Colori:</strong> Rosso e oro</p>
                </div>
            </div>

            <!-- Serpeverde -->
            <div class="col-12 col-md-6 col-lg-3 mb-4">
                <div class="bg-success text-white p-4 h-100">
                    <h3>🐍 Serpeverde</h3>
                    <p><strong>Fondatore:</strong> Salazar Serpeverde</p>
                    <p><strong>Valori:</strong> Astuzia, ambizione</p>
                    <p><strong>Colori:</strong> Verde e argento</p>
                </div>
            </div>

            <!-- Tassorosso -->
            <div class="col-12 col-md-6 col-lg-3 mb-4">
                <div class="bg-warning p-4 h-100">
                    <h3>🦡 Tassorosso</h3>
                    <p><strong>Fondatore:</strong> Tosca Tassorosso</p>
                    <p><strong>Valori:</strong> Lealtà, pazienza</p>
                    <p><strong>Colori:</strong> Giallo e nero</p>
                </div>
            </div>

            <!-- Corvonero -->
            <div class="col-12 col-md-6 col-lg-3 mb-4">
                <div class="bg-primary text-white p-4 h-100">
                    <h3>🦅 Corvonero</h3>
                    <p><strong>Fondatore:</strong> Corinna Corvonero</p>
                    <p><strong>Valori:</strong> Intelligenza, creatività</p>
                    <p><strong>Colori:</strong> Blu e bronzo</p>
                </div>
            </div>

        </div>

        <hr class="my-5">

        <!-- Layout Sidebar + Contenuto -->
        <div class="row">

            <!-- Sidebar (1/4 su desktop, full su mobile) -->
            <div class="col-12 col-lg-3 mb-4">
                <div class="bg-light p-3">
                    <h4>Menu</h4>
                    <ul class="list-unstyled">
                        <li><a href="#">Storia</a></li>
                        <li><a href="#">Materie</a></li>
                        <li><a href="#">Professori</a></li>
                        <li><a href="#">Regole</a></li>
                    </ul>
                </div>
            </div>

            <!-- Contenuto Principale (3/4 su desktop, full su mobile) -->
            <div class="col-12 col-lg-9">
                <h2>Storia di Hogwarts</h2>
                <p>
                    Hogwarts fu fondata oltre mille anni fa dai quattro maghi più potenti
                    dell'epoca: Godric Grifondoro, Salazar Serpeverde, Tosca Tassorosso
                    e Corinna Corvonero.
                </p>
                <p>
                    Ognuno di loro creò una casa che rifletteva i propri valori e cercava
                    studenti con qualità simili. Il Cappello Parlante fu creato per continuare
                    lo smistamento anche dopo la loro morte.
                </p>

                <!-- Sottogrid: 2 colonne -->
                <div class="row mt-4">
                    <div class="col-12 col-md-6 mb-3">
                        <div class="border p-3">
                            <h5>Il Cappello Parlante</h5>
                            <p>Smista ogni nuovo studente nella casa più adatta.</p>
                        </div>
                    </div>
                    <div class="col-12 col-md-6 mb-3">
                        <div class="border p-3">
                            <h5>La Coppa delle Case</h5>
                            <p>Ogni anno si assegnano punti per premiare la casa vincitrice.</p>
                        </div>
                    </div>
                </div>
            </div>

        </div>

    </div>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

## 🎯 Altre Classi Utili

### Auto-width Columns

```html
<div class="row">
    <div class="col">Auto</div>
    <div class="col">Auto</div>
    <div class="col">Auto</div>
</div>
```
Le colonne si dividono automaticamente lo spazio.

### Mix Auto + Fixed

```html
<div class="row">
    <div class="col">Flessibile</div>
    <div class="col-6">Fissa (metà)</div>
    <div class="col">Flessibile</div>
</div>
```

### Offset (Spostare Colonne)

```html
<div class="row">
    <div class="col-4 offset-4">
        Centrata (4 unità, spostata di 4)
    </div>
</div>
```

### Gutters (Spazio tra colonne)

```html
<!-- Nessuno spazio -->
<div class="row g-0">
    <div class="col">No gap</div>
    <div class="col">No gap</div>
</div>

<!-- Spazio grande -->
<div class="row g-4">
    <div class="col">Gap grande</div>
    <div class="col">Gap grande</div>
</div>
```

### Allineamento Verticale

```html
<div class="row align-items-start">Allineato in alto</div>
<div class="row align-items-center">Allineato al centro</div>
<div class="row align-items-end">Allineato in basso</div>
```

### Ordine Colonne

```html
<div class="row">
    <div class="col order-3">Terzo (ma scritto primo)</div>
    <div class="col order-1">Primo</div>
    <div class="col order-2">Secondo</div>
</div>
```

## 🏆 Challenge: Layout Completo Hogwarts

Crea una pagina `case.html` con un layout completo!

**Requisiti:**
1. Header a tutta larghezza con titolo
2. Sezione "Le Case":
   - 4 colonne su desktop (`col-lg-3`)
   - 2 colonne su tablet (`col-md-6`)
   - 1 colonna su mobile (`col-12`)
   - Ogni colonna ha sfondo diverso per casa
3. Sezione "Informazioni":
   - Sidebar sinistra 25% (`col-lg-3`)
   - Contenuto principale 75% (`col-lg-9`)
   - Entrambe full-width su mobile
4. Sezione "Professori":
   - 3 card in riga su desktop (`col-lg-4`)
   - 1 per riga su mobile
5. Footer centrato

<details>
<summary>💡 Clicca per vedere la soluzione</summary>

```html
<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hogwarts - Le Case</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>

    <!-- Header -->
    <div class="bg-dark text-white text-center p-5">
        <h1>Scuola di Magia di Hogwarts</h1>
        <p class="lead">Draco Dormiens Nunquam Titillandus</p>
    </div>

    <!-- Sezione Case -->
    <div class="container my-5">
        <h2 class="text-center mb-4">Le Quattro Case</h2>

        <div class="row">
            <div class="col-12 col-md-6 col-lg-3 mb-3">
                <div class="bg-danger text-white p-4 text-center">
                    <h3>🦁 Grifondoro</h3>
                    <p>Coraggio e audacia</p>
                </div>
            </div>
            <div class="col-12 col-md-6 col-lg-3 mb-3">
                <div class="bg-success text-white p-4 text-center">
                    <h3>🐍 Serpeverde</h3>
                    <p>Astuzia e ambizione</p>
                </div>
            </div>
            <div class="col-12 col-md-6 col-lg-3 mb-3">
                <div class="bg-warning p-4 text-center">
                    <h3>🦡 Tassorosso</h3>
                    <p>Lealtà e pazienza</p>
                </div>
            </div>
            <div class="col-12 col-md-6 col-lg-3 mb-3">
                <div class="bg-primary text-white p-4 text-center">
                    <h3>🦅 Corvonero</h3>
                    <p>Intelligenza e saggezza</p>
                </div>
            </div>
        </div>
    </div>

    <hr>

    <!-- Sezione Informazioni (Sidebar + Content) -->
    <div class="container my-5">
        <div class="row">

            <!-- Sidebar -->
            <div class="col-12 col-lg-3 mb-4">
                <div class="bg-light p-3">
                    <h4>Navigazione</h4>
                    <ul class="list-unstyled">
                        <li><a href="#">Le Case</a></li>
                        <li><a href="#">Professori</a></li>
                        <li><a href="#">Materie</a></li>
                        <li><a href="#">Storia</a></li>
                    </ul>
                </div>
            </div>

            <!-- Content -->
            <div class="col-12 col-lg-9">
                <h2>Storia delle Case</h2>
                <p>
                    Le quattro case furono create dai fondatori di Hogwarts per
                    raggruppare studenti con caratteristiche simili.
                </p>
                <p>
                    Ogni casa ha il proprio dormitorio, sala comune e fantasma.
                    Gli studenti guadagnano punti per la loro casa durante l'anno.
                </p>
            </div>

        </div>
    </div>

    <hr>

    <!-- Sezione Professori -->
    <div class="container my-5">
        <h2 class="text-center mb-4">I Nostri Professori</h2>

        <div class="row">
            <div class="col-12 col-lg-4 mb-4">
                <div class="border p-4 text-center">
                    <h4>Albus Silente</h4>
                    <p><strong>Materia:</strong> Preside</p>
                    <p>Il mago più potente del mondo</p>
                </div>
            </div>
            <div class="col-12 col-lg-4 mb-4">
                <div class="border p-4 text-center">
                    <h4>Minerva McGranitt</h4>
                    <p><strong>Materia:</strong> Trasfigurazione</p>
                    <p>Vice-preside e capo Grifondoro</p>
                </div>
            </div>
            <div class="col-12 col-lg-4 mb-4">
                <div class="border p-4 text-center">
                    <h4>Severus Piton</h4>
                    <p><strong>Materia:</strong> Pozioni</p>
                    <p>Maestro di Pozioni e capo Serpeverde</p>
                </div>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <div class="bg-dark text-white text-center p-4">
        <p>&copy; 2024 Hogwarts - Tutti i diritti riservati</p>
    </div>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```
</details>

## 💡 Tips & Tricks

### Debug del Grid

Aggiungi bordi temporanei per vedere le colonne:

```html
<div class="col-6 border">
    Vedo i bordi!
</div>
```

### Altezza Uguale

Per box di altezza uguale in una riga:

```html
<div class="row">
    <div class="col-4">
        <div class="h-100 bg-primary text-white p-3">
            Stessa altezza
        </div>
    </div>
    <div class="col-4">
        <div class="h-100 bg-success text-white p-3">
            Anche questo<br>anche se<br>ha più testo
        </div>
    </div>
</div>
```

### Mobile First

Pensa prima al mobile, poi aggiungi le classi per schermi più grandi:

```html
<!-- Prima mobile (col-12), poi tablet (col-md-6), poi desktop (col-lg-4) -->
<div class="col-12 col-md-6 col-lg-4">
    Mobile first!
</div>
```

## ✅ Checklist: Cosa hai imparato

- [ ] Capisco il sistema a 12 colonne
- [ ] So usare `row` e `col`
- [ ] So creare colonne di dimensioni specifiche (`col-6`, `col-4`, ecc.)
- [ ] Conosco i breakpoints (sm, md, lg, xl)
- [ ] So creare layout responsive
- [ ] So usare offset e gutters
- [ ] Ho completato il challenge del Layout Hogwarts

## 📚 Schema Veloce

```
Container (centra e contiene)
  └── Row (riga orizzontale)
        ├── Col (colonna 1/12)
        ├── Col (colonna 1/12)
        └── Col (colonna 1/12)
```

## 🎯 Prossimi Passi

Eccellente! Ora sai creare layout complessi con il Grid System!

Nella [prossima lezione](06-bootstrap-componenti.md) impareremo i **componenti Bootstrap**: card, navbar, modal, e molto altro!

---

*"L'ordine è la chiave della magia, proprio come il Grid è la chiave di un layout perfetto!"* - Hermione (forse!)

Sei sulla strada giusta! Continua così! 🌟
