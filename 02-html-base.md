# Lezione 2: HTML Base - Tag Fondamentali

Benvenuto alla seconda lezione! Oggi impareremo i tag HTML più importanti che userai tutti i giorni. È come imparare gli incantesimi base prima di passare a quelli avanzati!

## 🎯 Obiettivi della Lezione

Alla fine di questa lezione saprai:
- Creare liste ordinate e non ordinate
- Inserire link e immagini
- Formattare il testo (grassetto, corsivo, sottolineato)
- Usare divisori e linee orizzontali

## 🧙 Concetti Fondamentali

### I Mattoni del Web

Nella lezione precedente hai imparato la struttura base. Ora imparerai i **mattoni fondamentali** che userai per costruire qualsiasi sito web.

Pensa ai tag HTML come agli **incantesimi base** che ogni mago deve conoscere:
- `Lumos` (luce) è fondamentale → `<a>` (link) è fondamentale
- `Wingardium Leviosa` (levitazione) è essenziale → `<img>` (immagine) è essenziale
- Gli incantesimi complessi combinano quelli base → Le pagine web combinano tag semplici!

### Tag di Formattazione Testo

Prima di tutto, vediamo come dare **stile** al testo:

```html
<p>Testo normale</p>
<p><strong>Testo in grassetto</strong></p>
<p><em>Testo in corsivo</em></p>
<p><u>Testo sottolineato</u></p>
<p><mark>Testo evidenziato</mark></p>
<p><small>Testo piccolo</small></p>
```

### Le Liste

Le liste sono super utili! Ne esistono di due tipi:

**Liste non ordinate** (con pallini):
```html
<ul>
    <li>Grifondoro</li>
    <li>Serpeverde</li>
    <li>Tassorosso</li>
    <li>Corvonero</li>
</ul>
```

**Liste ordinate** (con numeri):
```html
<ol>
    <li>Primo anno: Pietre Filosofale</li>
    <li>Secondo anno: Camera dei Segreti</li>
    <li>Terzo anno: Prigioniero di Azkaban</li>
</ol>
```

## ⚡ Analogia Harry Potter

Pensa ai tag HTML come agli **strumenti di un mago**:

- `<a>` (link) = **Passaporta** → Ti porta in un altro posto
- `<img>` (immagine) = **Foto del Profeta** → Mostra immagini (anche animate!)
- `<ul>` / `<ol>` (liste) = **Lista di Materiale Scolastico** → Organizzare informazioni
- `<strong>` (grassetto) = **Incantesimo Sonorus** → Rende il testo più forte/importante
- `<br>` (a capo) = **Finite Incantatem** → Interrompe e va a capo

## 💻 Link - Il Tag `<a>`

Il tag anchor (`<a>`) è uno dei più importanti. Serve per creare **collegamenti**.

### Link a un altro sito
```html
<a href="https://www.google.com">Vai su Google</a>
```

### Link che apre in una nuova scheda
```html
<a href="https://www.google.com" target="_blank">Apri Google in nuova scheda</a>
```

### Link a un'altra pagina del tuo sito
```html
<a href="pozioni.html">Vai alla pagina Pozioni</a>
```

**Parti del tag `<a>`:**
- `href` = "Hyper Reference" → dove vuoi andare
- `target="_blank"` = apri in nuova scheda
- Il testo tra `<a>` e `</a>` = quello che si vede cliccabile

## 🖼️ Immagini - Il Tag `<img>`

Le immagini rendono il sito molto più bello!

```html
<img src="bacchetta.jpg" alt="La bacchetta di Harry Potter">
```

**Parti del tag `<img>`:**
- `src` = "source" → il percorso/nome dell'immagine
- `alt` = "alternative text" → descrizione dell'immagine (importante!)

### Modificare dimensioni
```html
<img src="bacchetta.jpg" alt="Bacchetta" width="300">
<img src="bacchetta.jpg" alt="Bacchetta" height="200">
<img src="bacchetta.jpg" alt="Bacchetta" width="300" height="200">
```

### Immagini da internet
```html
<img src="https://esempio.com/hogwarts.jpg" alt="Castello di Hogwarts">
```

## 🎨 Esempio Harry Potter Completo

Ecco una pagina completa che usa tutti questi tag:

```html
<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Guida di Hogwarts</title>
</head>
<body>
    <h1>Benvenuto alla Scuola di Magia di Hogwarts</h1>

    <p>
        Hogwarts è la scuola di magia più <strong>prestigiosa</strong>
        del mondo magico. Qui imparerai <em>incantesimi incredibili</em>!
    </p>

    <hr>

    <h2>Le Quattro Case</h2>
    <ul>
        <li><strong>Grifondoro</strong> - Il coraggio sopra ogni cosa</li>
        <li><strong>Serpeverde</strong> - L'astuzia e l'ambizione</li>
        <li><strong>Tassorosso</strong> - La lealtà e il duro lavoro</li>
        <li><strong>Corvonero</strong> - L'intelligenza e la saggezza</li>
    </ul>

    <hr>

    <h2>Programma del Primo Anno</h2>
    <ol>
        <li>Pozioni con il Professor Piton</li>
        <li>Trasfigurazione con la Prof.ssa McGranitt</li>
        <li>Incantesimi con il Prof. Vitious</li>
        <li>Difesa contro le Arti Oscure</li>
        <li>Erbologia con la Prof.ssa Sprite</li>
    </ol>

    <hr>

    <h2>Link Utili</h2>
    <p>
        <a href="https://www.google.com" target="_blank">Cerca informazioni su Google</a><br>
        <a href="orario.html">Vedi l'orario delle lezioni</a><br>
        <a href="mappa.html">Mappa del castello</a>
    </p>

    <hr>

    <h2>Il Castello</h2>
    <p>Ecco una <mark>bellissima immagine</mark> del castello:</p>
    <!-- Nota: sostituisci con un vero link a un'immagine -->
    <img src="hogwarts-castello.jpg" alt="Il castello di Hogwarts" width="500">

    <hr>

    <h3>Note Importanti</h3>
    <p>
        <small>La Foresta Proibita è off-limits per tutti gli studenti.</small><br>
        <small>Coprifuoco alle 22:00 per tutti gli anni.</small>
    </p>

    <p>
        Per qualsiasi domanda, contatta il <strong>Preside Albus Silente</strong>.
    </p>
</body>
</html>
```

## 🛠️ Come Aggiungere Immagini al Tuo Progetto

### Opzione 1: Immagini dalla stessa cartella
1. Scarica un'immagine (es: `hogwarts.jpg`)
2. Mettila nella **stessa cartella** del tuo file `.html`
3. Usa: `<img src="hogwarts.jpg" alt="Hogwarts">`

### Opzione 2: Immagini in una sottocartella
1. Crea una cartella chiamata `immagini`
2. Metti le immagini dentro
3. Usa: `<img src="immagini/hogwarts.jpg" alt="Hogwarts">`

### Opzione 3: Immagini da Internet
1. Trova un'immagine online
2. Click destro > "Copia indirizzo immagine"
3. Usa: `<img src="https://url-completo-immagine.jpg" alt="Descrizione">`

## 🏆 Challenge: Pagina delle Pozioni

Crea una pagina `pozioni.html` che contiene:

**Requisiti:**
1. Titolo principale: "Libro delle Pozioni"
2. Sottotitolo: "Primo Anno"
3. Paragrafo introduttivo con testo in **grassetto** e *corsivo*
4. Una lista **non ordinata** con 4 pozioni (es: Felix Felicis, Veritaserum, ecc.)
5. Una lista **ordinata** con 3 ingredienti di una pozione
6. Un link a Google che apre in nuova scheda
7. Una linea orizzontale (`<hr>`) per dividere sezioni
8. Un'immagine di una pozione (usa un'immagine da internet)

<details>
<summary>💡 Clicca qui per vedere una soluzione possibile</summary>

```html
<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Libro delle Pozioni</title>
</head>
<body>
    <h1>Libro delle Pozioni</h1>
    <h2>Primo Anno - Professor Piton</h2>

    <p>
        Le pozioni sono una <strong>parte fondamentale</strong> della magia.
        Richiedono <em>precisione assoluta</em> e <em>pazienza infinita</em>.
    </p>

    <hr>

    <h3>Pozioni che Studieremo</h3>
    <ul>
        <li>Pozione Rigonfiante</li>
        <li>Filtro della Pace</li>
        <li>Pozione Calderone Fuso</li>
        <li>Antidoto ai Veleni Comuni</li>
    </ul>

    <hr>

    <h3>Ricetta: Pozione Rigonfiante</h3>
    <p>Segui questi passi <strong>nell'ordine esatto</strong>:</p>
    <ol>
        <li>Aggiungi 3 occhi di scarafaggio essiccati</li>
        <li>Mescola 7 volte in senso orario</li>
        <li>Aggiungi 2 gocce di veleno di serpente</li>
        <li>Lascia sobbollire per 10 minuti</li>
    </ol>

    <hr>

    <h3>Approfondimenti</h3>
    <p>
        <a href="https://www.google.com/search?q=pozioni+harry+potter" target="_blank">
            Cerca altre pozioni su Google
        </a>
    </p>

    <hr>

    <h3>Calderone Magico</h3>
    <img src="https://images.unsplash.com/photo-1603048588665-791ca8aea617?w=400"
         alt="Calderone con pozione"
         width="400">

    <hr>

    <p>
        <small>Attenzione: Maneggiare le pozioni con cura.
        Il Professor Piton non tollera errori!</small>
    </p>
</body>
</html>
```
</details>

## 💡 Tips & Tricks

### Trucchi per le Liste

**Liste annidate** (una lista dentro un'altra):
```html
<ul>
    <li>Grifondoro
        <ul>
            <li>Harry Potter</li>
            <li>Hermione Granger</li>
            <li>Ron Weasley</li>
        </ul>
    </li>
    <li>Serpeverde
        <ul>
            <li>Draco Malfoy</li>
            <li>Pansy Parkinson</li>
        </ul>
    </li>
</ul>
```

### Andare a Capo

Per andare a capo senza creare un nuovo paragrafo:
```html
<p>
    Prima riga<br>
    Seconda riga<br>
    Terza riga
</p>
```

### Link Email

Per creare un link che apre l'email:
```html
<a href="mailto:hogwarts@magic.com">Contattaci via email</a>
```

### Linea Orizzontale

Per dividere visivamente sezioni:
```html
<hr>
```

### Commenti Utili

Usa i commenti per organizzare il codice:
```html
<!-- ==== SEZIONE HERO ==== -->
<h1>Titolo Principale</h1>

<!-- ==== SEZIONE LISTA CASE ==== -->
<ul>
    <li>Grifondoro</li>
    <li>Serpeverde</li>
</ul>
```

## 🐛 Errori Comuni da Evitare

### ❌ Errore 1: Dimenticare l'attributo alt nelle immagini
```html
<!-- SBAGLIATO -->
<img src="foto.jpg">

<!-- GIUSTO -->
<img src="foto.jpg" alt="Descrizione foto">
```

### ❌ Errore 2: Dimenticare le virgolette
```html
<!-- SBAGLIATO -->
<a href=pagina.html>Link</a>

<!-- GIUSTO -->
<a href="pagina.html">Link</a>
```

### ❌ Errore 3: Non chiudere i tag delle liste
```html
<!-- SBAGLIATO -->
<ul>
    <li>Elemento 1
    <li>Elemento 2
</ul>

<!-- GIUSTO -->
<ul>
    <li>Elemento 1</li>
    <li>Elemento 2</li>
</ul>
```

### ❌ Errore 4: Mettere un div dentro un p
```html
<!-- SBAGLIATO -->
<p><div>Testo</div></p>

<!-- GIUSTO -->
<div><p>Testo</p></div>
```

## ✅ Checklist: Cosa hai imparato

Segna quello che hai capito:

- [ ] So creare liste ordinate con `<ol>`
- [ ] So creare liste non ordinate con `<ul>`
- [ ] So aggiungere link con `<a href="">`
- [ ] So inserire immagini con `<img src="" alt="">`
- [ ] So formattare il testo (grassetto, corsivo)
- [ ] So usare `<br>` per andare a capo
- [ ] So usare `<hr>` per linee orizzontali
- [ ] Ho completato la challenge della pagina Pozioni

## 📚 Riepilogo Tag Imparati

| Tag | Cosa fa | Esempio |
|-----|---------|---------|
| `<strong>` | Testo in grassetto | `<strong>Importante</strong>` |
| `<em>` | Testo in corsivo | `<em>Enfatizzato</em>` |
| `<u>` | Testo sottolineato | `<u>Sottolineato</u>` |
| `<mark>` | Testo evidenziato | `<mark>Evidenziato</mark>` |
| `<small>` | Testo piccolo | `<small>Piccolo</small>` |
| `<ul>` | Lista non ordinata | Con pallini |
| `<ol>` | Lista ordinata | Con numeri |
| `<li>` | Elemento lista | Va dentro `<ul>` o `<ol>` |
| `<a>` | Link/collegamento | `<a href="...">Testo</a>` |
| `<img>` | Immagine | `<img src="..." alt="...">` |
| `<br>` | A capo | Nessuna chiusura |
| `<hr>` | Linea orizzontale | Nessuna chiusura |

## 🎯 Prossimi Passi

Fantastico lavoro! Ora sai usare i tag HTML fondamentali.

Nella [prossima lezione](03-html-form.md) impareremo a creare **form interattivi**: moduli di iscrizione, quiz, e altro!

Prima di proseguire, prova a:
1. Completare la challenge della pagina Pozioni
2. Creare una tua pagina personalizzata con tutti i tag che hai imparato
3. Sperimentare con liste annidate e combinazioni di tag

---

*"La differenza tra l'ordinario e lo straordinario è la pratica."* - Hermione Granger (più o meno!)

Continua a praticare e diventerai un mago del web! 🪄
