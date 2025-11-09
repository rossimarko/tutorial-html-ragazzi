# Lezione 4: Bootstrap Setup - Dai Stile al Tuo Sito!

Benvenuto alla quarta lezione! Oggi scoprirai Bootstrap, uno strumento magico che renderà il tuo sito bellissimo senza scrivere CSS!

## 🎯 Obiettivi della Lezione

Alla fine di questa lezione saprai:
- Cos'è Bootstrap e perché è utile
- Come installare Bootstrap 5 con CDN
- Usare le classi base di Bootstrap
- Creare pulsanti, colori e spaziature
- Costruire il tuo primo sito con Bootstrap

## 🧙 Concetti Fondamentali

### Cos'è Bootstrap?

**Bootstrap** è un framework CSS: una **collezione pronta di stili** che puoi usare semplicemente aggiungendo delle classi HTML.

Invece di scrivere CSS da zero per ogni elemento, usi le classi di Bootstrap e... BAM! Tutto diventa bello automaticamente!

**Esempio senza Bootstrap:**
```html
<!-- Devi scrivere CSS a mano -->
<button style="background-color: blue; color: white; padding: 10px; border-radius: 5px;">
    Clicca qui
</button>
```

**Esempio CON Bootstrap:**
```html
<!-- Aggiungi solo una classe! -->
<button class="btn btn-primary">Clicca qui</button>
```

Molto più semplice, vero?

### Perché usare Bootstrap?

1. **Veloce** - Non devi scrivere CSS da zero
2. **Bello** - Design professionale già pronto
3. **Responsive** - Funziona su telefono, tablet, PC
4. **Compatibile** - Funziona su tutti i browser
5. **Documentazione** - Tantissimi esempi pronti da copiare!

## ⚡ Analogia Harry Potter

Pensa a Bootstrap come a **Olivander** (il negozio di bacchette):

- **Senza Bootstrap** = Costruire la bacchetta da zero, tagliando il legno, cercando il nucleo magico, ecc.
- **Con Bootstrap** = Andare da Olivander e scegliere tra bacchette già pronte e perfette!

Bootstrap ti fornisce componenti già pronti (bottoni, card, navbar) come Olivander ti dà bacchette già fatte. Tu scegli quella giusta e la usi!

Ogni **classe Bootstrap** è come un **incantesimo**:
- `btn btn-primary` = Crea un bottone blu
- `alert alert-success` = Crea un messaggio verde di successo
- `card` = Crea una card bellissima

## 💻 Come Installare Bootstrap

Ci sono 2 modi per usare Bootstrap. Noi useremo il più semplice: **CDN**.

### Metodo 1: CDN (Consigliato per iniziare)

**CDN** = Content Delivery Network → Carichi Bootstrap da Internet

Copia e incolla questi link nella tua pagina HTML:

```html
<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Il Mio Sito Bootstrap</title>

    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>

    <h1>Ciao Bootstrap!</h1>

    <!-- Bootstrap JavaScript (opzionale, serve per componenti interattivi) -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

**Dove mettere i link:**
- CSS di Bootstrap → Dentro `<head>` prima della chiusura
- JS di Bootstrap → Alla fine del `<body>` prima della chiusura

### Template Base Bootstrap

Ecco il template completo da usare sempre:

```html
<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hogwarts - Sito Ufficiale</title>

    <!-- Bootstrap 5.3.3 CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>

    <!-- Contenuto qui -->
    <div class="container">
        <h1>Benvenuto a Hogwarts</h1>
        <p>Questo è un sito creato con Bootstrap!</p>
    </div>

    <!-- Bootstrap JS -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

## 🎨 Prime Classi Bootstrap

### Container

La classe `container` centra il contenuto e gli dà margini:

```html
<div class="container">
    <h1>Titolo</h1>
    <p>Testo centrato e con margini belli</p>
</div>
```

Esiste anche `container-fluid` che occupa tutta la larghezza:

```html
<div class="container-fluid">
    <h1>Questo occupa tutta la larghezza</h1>
</div>
```

### Pulsanti

Bootstrap ha pulsanti bellissimi!

```html
<!-- Pulsanti con colori -->
<button class="btn btn-primary">Primario (blu)</button>
<button class="btn btn-secondary">Secondario (grigio)</button>
<button class="btn btn-success">Successo (verde)</button>
<button class="btn btn-danger">Pericolo (rosso)</button>
<button class="btn btn-warning">Attenzione (giallo)</button>
<button class="btn btn-info">Info (azzurro)</button>
<button class="btn btn-light">Chiaro</button>
<button class="btn btn-dark">Scuro</button>

<!-- Pulsanti grandi e piccoli -->
<button class="btn btn-primary btn-lg">Grande</button>
<button class="btn btn-primary">Normale</button>
<button class="btn btn-primary btn-sm">Piccolo</button>
```

### Colori Testo

```html
<p class="text-primary">Testo blu</p>
<p class="text-success">Testo verde</p>
<p class="text-danger">Testo rosso</p>
<p class="text-warning">Testo giallo</p>
<p class="text-muted">Testo grigio chiaro</p>
```

### Colori Sfondo

```html
<div class="bg-primary text-white p-3">Sfondo blu</div>
<div class="bg-success text-white p-3">Sfondo verde</div>
<div class="bg-danger text-white p-3">Sfondo rosso</div>
<div class="bg-warning p-3">Sfondo giallo</div>
<div class="bg-light p-3">Sfondo chiaro</div>
<div class="bg-dark text-white p-3">Sfondo scuro</div>
```

### Spaziature

**Padding** (spazio interno):
- `p-1` → `p-5` = Padding su tutti i lati
- `pt-3` = Padding top (sopra)
- `pb-3` = Padding bottom (sotto)
- `ps-3` = Padding start (sinistra)
- `pe-3` = Padding end (destra)

**Margin** (spazio esterno):
- `m-1` → `m-5` = Margin su tutti i lati
- `mt-3` = Margin top
- `mb-3` = Margin bottom
- `ms-3` = Margin start
- `me-3` = Margin end

```html
<div class="p-3 m-2 bg-primary text-white">
    Box con padding 3 e margin 2
</div>

<div class="pt-5 pb-2">
    Padding sopra 5, sotto 2
</div>
```

### Allineamento Testo

```html
<p class="text-start">Testo a sinistra</p>
<p class="text-center">Testo centrato</p>
<p class="text-end">Testo a destra</p>
```

## 🎨 Esempio Harry Potter Completo

```html
<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Scuola di Hogwarts</title>

    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>

    <!-- Header -->
    <div class="bg-dark text-white text-center p-5">
        <h1>Scuola di Magia e Stregoneria di Hogwarts</h1>
        <p class="lead">Draco Dormiens Nunquam Titillandus</p>
    </div>

    <!-- Contenuto -->
    <div class="container mt-5">

        <!-- Intro -->
        <h2 class="text-center mb-4">Benvenuto al Primo Anno</h2>
        <p class="text-center text-muted">
            Preparati a vivere l'avventura più magica della tua vita!
        </p>

        <hr class="my-5">

        <!-- Le Case -->
        <h3 class="mb-3">Le Quattro Case di Hogwarts</h3>

        <div class="row">
            <!-- Grifondoro -->
            <div class="col-12 mb-3">
                <div class="bg-danger text-white p-4">
                    <h4>🦁 Grifondoro</h4>
                    <p>Coraggio, cavalleria e determinazione</p>
                    <button class="btn btn-light">Scopri di più</button>
                </div>
            </div>

            <!-- Serpeverde -->
            <div class="col-12 mb-3">
                <div class="bg-success text-white p-4">
                    <h4>🐍 Serpeverde</h4>
                    <p>Astuzia, ambizione e ingegno</p>
                    <button class="btn btn-light">Scopri di più</button>
                </div>
            </div>

            <!-- Tassorosso -->
            <div class="col-12 mb-3">
                <div class="bg-warning p-4">
                    <h4>🦡 Tassorosso</h4>
                    <p>Lealtà, dedizione e pazienza</p>
                    <button class="btn btn-dark">Scopri di più</button>
                </div>
            </div>

            <!-- Corvonero -->
            <div class="col-12 mb-3">
                <div class="bg-primary text-white p-4">
                    <h4>🦅 Corvonero</h4>
                    <p>Intelligenza, creatività e saggezza</p>
                    <button class="btn btn-light">Scopri di più</button>
                </div>
            </div>
        </div>

        <hr class="my-5">

        <!-- Pulsanti azione -->
        <div class="text-center">
            <h3 class="mb-4">Inizia la Tua Avventura</h3>
            <button class="btn btn-primary btn-lg me-2">📜 Iscriviti Ora</button>
            <button class="btn btn-secondary btn-lg">📖 Leggi di Più</button>
        </div>

        <hr class="my-5">

        <!-- Alert -->
        <div class="alert alert-warning">
            <strong>Attenzione!</strong> Le lezioni iniziano il 1° Settembre. Non dimenticare il materiale!
        </div>

        <div class="alert alert-success">
            <strong>Ottimo!</strong> La tua candidatura è stata accettata!
        </div>

    </div>

    <!-- Footer -->
    <div class="bg-dark text-white text-center p-4 mt-5">
        <p class="mb-0">&copy; 2024 Hogwarts School of Witchcraft and Wizardry</p>
        <small class="text-muted">Tutti i diritti riservati</small>
    </div>

    <!-- Bootstrap JS -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

## 🏆 Challenge: Pagina Materiale Scolastico

Crea una pagina `materiale.html` per la lista del materiale scolastico di Hogwarts usando Bootstrap!

**Requisiti:**
1. Header con sfondo scuro (`bg-dark`) e testo bianco
2. Container per il contenuto
3. Titolo centrato "Materiale Primo Anno"
4. 3 sezioni con sfondo colorato (usa `bg-primary`, `bg-success`, `bg-warning`):
   - Libri (lista di 3 libri)
   - Abbigliamento (lista di 3 capi)
   - Oggetti Magici (lista di 3 oggetti)
5. Ogni sezione deve avere padding (`p-4`) e margine bottom (`mb-3`)
6. Un pulsante grande "Acquista su Diagon Alley" centrato
7. Un alert di avviso (giallo) con info importanti
8. Footer con sfondo scuro

<details>
<summary>💡 Clicca per vedere una soluzione</summary>

```html
<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Materiale Scolastico - Hogwarts</title>

    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>

    <!-- Header -->
    <div class="bg-dark text-white text-center p-5">
        <h1>📚 Materiale Scolastico</h1>
        <p>Primo Anno - Hogwarts</p>
    </div>

    <!-- Container -->
    <div class="container my-5">

        <h2 class="text-center mb-5">Lista Materiale Obbligatorio</h2>

        <!-- Sezione Libri -->
        <div class="bg-primary text-white p-4 mb-3">
            <h3>📖 Libri di Testo</h3>
            <ul>
                <li>Storia di Hogwarts - Bathilda Bath</li>
                <li>Libro Standard degli Incantesimi (Livello 1)</li>
                <li>Mille Erbe e Funghi Magici</li>
            </ul>
        </div>

        <!-- Sezione Abbigliamento -->
        <div class="bg-success text-white p-4 mb-3">
            <h3>👔 Abbigliamento</h3>
            <ul>
                <li>3 Vesti da lavoro semplici (nere)</li>
                <li>1 Cappello a punta (nero)</li>
                <li>1 Paio di guanti protettivi (pelle di drago o simile)</li>
            </ul>
        </div>

        <!-- Sezione Oggetti Magici -->
        <div class="bg-warning p-4 mb-3">
            <h3>🪄 Oggetti Magici</h3>
            <ul>
                <li>1 Bacchetta magica</li>
                <li>1 Calderone di peltro (dimensione standard 2)</li>
                <li>1 Set di fiale di vetro</li>
            </ul>
        </div>

        <!-- Alert -->
        <div class="alert alert-warning mt-4">
            <strong>Importante!</strong> Tutto il materiale può essere acquistato a Diagon Alley.
            Gli studenti del primo anno NON possono portare scope personali.
        </div>

        <!-- Pulsante -->
        <div class="text-center mt-5">
            <button class="btn btn-primary btn-lg">🛒 Acquista su Diagon Alley</button>
        </div>

    </div>

    <!-- Footer -->
    <div class="bg-dark text-white text-center p-4">
        <p class="mb-0">Hogwarts School - Ufficio Materiale</p>
        <small>Per domande contatta l'amministrazione</small>
    </div>

    <!-- Bootstrap JS -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```
</details>

## 💡 Tips & Tricks

### Ispezionare gli Elementi

Usa gli strumenti sviluppatore del browser per vedere le classi Bootstrap:
1. Click destro su un elemento
2. "Ispeziona" o "Inspect"
3. Vedi tutte le classi CSS applicate!

### Combinare Classi

Puoi usare più classi insieme:

```html
<button class="btn btn-primary btn-lg mt-3 mb-2">
    Pulsante grande blu con margini
</button>
```

### Classi Utility Utili

```html
<!-- Bordi arrotondati -->
<div class="rounded">Angoli arrotondati</div>
<div class="rounded-circle">Cerchio perfetto (per foto profilo)</div>

<!-- Ombra -->
<div class="shadow">Box con ombra leggera</div>
<div class="shadow-lg">Box con ombra grande</div>

<!-- Display -->
<div class="d-none">Nascosto</div>
<div class="d-block">Visibile come blocco</div>

<!-- Bordi -->
<div class="border">Con bordo</div>
<div class="border border-primary">Bordo blu</div>
```

### Responsive

Puoi rendere le classi responsive:

```html
<!-- Nascosto su mobile, visibile su desktop -->
<div class="d-none d-md-block">Solo su schermi grandi</div>

<!-- Padding diverso su mobile e desktop -->
<div class="p-2 p-md-5">Padding piccolo su mobile, grande su desktop</div>
```

## 🐛 Errori Comuni

### ❌ Errore 1: Dimenticare il CDN
Se Bootstrap non funziona, controlla di aver messo il link CSS!

### ❌ Errore 2: CDN nel posto sbagliato
```html
<!-- SBAGLIATO - CSS nel body -->
<body>
    <link href="bootstrap.css">
</body>

<!-- GIUSTO - CSS nell'head -->
<head>
    <link href="bootstrap.css">
</head>
```

### ❌ Errore 3: Nome classe sbagliato
```html
<!-- SBAGLIATO -->
<button class="button primary">Non funziona</button>

<!-- GIUSTO -->
<button class="btn btn-primary">Funziona!</button>
```

## ✅ Checklist: Cosa hai imparato

- [ ] So cos'è Bootstrap e perché è utile
- [ ] So installare Bootstrap con CDN
- [ ] So usare `container` e `container-fluid`
- [ ] So creare pulsanti con `btn` e colori
- [ ] Conosco le classi di colore (text, bg)
- [ ] So usare padding e margin (p-*, m-*)
- [ ] So allineare il testo (text-start, center, end)
- [ ] Ho completato la challenge del Materiale Scolastico

## 📚 Risorse Utili

- **Documentazione Bootstrap:** [getbootstrap.com](https://getbootstrap.com)
- Cerca "Bootstrap 5 [componente]" su Google per esempi
- Usa gli esempi della documentazione ufficiale

## 🎯 Prossimi Passi

Fantastico! Ora sai usare Bootstrap e le sue classi base!

Nella [prossima lezione](05-bootstrap-grid.md) impareremo il **Grid System**: il sistema che ti permette di creare layout complessi con righe e colonne!

---

*"Le pozioni richiedono precisione, così come Bootstrap richiede le classi giuste!"* - Professor Piton (forse!)

Hai fatto un ottimo lavoro! Continua così! 🪄
