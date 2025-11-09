# Lezione 1: Introduzione a HTML

Benvenuto alla tua prima lezione di magia... ehm, di Web Development! Preparati a scoprire come funziona il mondo dei siti web.

## 🎯 Obiettivi della Lezione

Alla fine di questa lezione saprai:
- Cos'è HTML e perché è importante
- Come funziona un sito web
- Cosa serve per creare la tua prima pagina
- La struttura base di un documento HTML

## 🧙 Concetti Fondamentali

### Cos'è HTML?

HTML sta per **HyperText Markup Language**. Non spaventarti per il nome! In pratica, HTML è il linguaggio che usiamo per dire al browser (Chrome, Firefox, ecc.) cosa mostrare sullo schermo.

Pensa a HTML come alle **istruzioni per costruire Hogwarts**. Se tu volessi costruire il castello, avresti bisogno di dire: "Qui va una torre, qui va una porta, qui va una finestra". HTML fa la stessa cosa, ma per i siti web!

Quando scrivi HTML, usi dei **tag** (etichette) che dicono al browser: "Questo è un titolo", "Questa è un'immagine", "Questo è un pulsante". Il browser legge le tue istruzioni e costruisce la pagina che vedi.

### Come funziona il Web?

Quando vai su un sito web, succedono queste cose:
1. **Tu** scrivi un indirizzo (es: www.hogwarts.com)
2. Il **browser** chiede al server: "Dammi la pagina di Hogwarts!"
3. Il **server** (un computer sempre acceso) risponde con file HTML, CSS, JavaScript
4. Il **browser** legge l'HTML e mostra la pagina sul tuo schermo

È come quando invii una civetta a Hogwarts per chiedere informazioni, e la civetta torna con una lettera di risposta!

## ⚡ Analogia Harry Potter

Immagina che **HTML** sia come la struttura del castello di Hogwarts:
- I **tag HTML** sono come i mattoni: `<h1>`, `<p>`, `<img>`, ecc.
- Un **documento HTML** è come il progetto completo del castello
- Il **browser** è come il costruttore che legge il progetto e costruisce il castello
- **Tu** sei l'architetto che decide dove va ogni cosa!

Proprio come Hogwarts ha:
- Torri (titoli grandi)
- Corridoi (paragrafi)
- Porte (link)
- Quadri (immagini)

Il tuo sito web avrà elementi HTML che corrispondono a tutte queste cose!

## 💻 Struttura Base di HTML

Ecco la struttura minima di OGNI pagina HTML. È come lo scheletro su cui costruirai tutto:

```html
<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Il mio primo sito magico</title>
</head>
<body>
    <h1>Benvenuto a Hogwarts!</h1>
    <p>Questa è la mia prima pagina web.</p>
</body>
</html>
```

**Spiegazione di ogni parte:**

- `<!DOCTYPE html>` - Dice al browser: "Ehi, questo è un file HTML5!"
- `<html>` - Contenitore principale, tutto va dentro qui
- `<head>` - Informazioni "invisibili" (titolo, impostazioni, ecc.)
- `<meta charset="UTF-8">` - Dice come leggere le lettere (serve per avere le lettere accentate)
- `<title>` - Il titolo che vedi nella scheda del browser
- `<body>` - Qui va tutto ciò che si VEDE sulla pagina
- `<h1>` - Titolo principale (Header 1)
- `<p>` - Paragrafo di testo

## 🛠️ Setup con Visual Studio Code

Segui questi passi per creare la tua prima pagina:

### Passo 1: Apri Visual Studio Code
- Avvia VS Code sul tuo computer

### Passo 2: Crea una nuova cartella
- File > Apri Cartella
- Crea una nuova cartella chiamata "il-mio-sito-hogwarts"
- Apri quella cartella in VS Code

### Passo 3: Crea il primo file HTML
- Click su "New File" (icona foglio in alto a sinistra)
- Chiamalo `index.html`
- Premi invio

### Passo 4: Usa il trucco magico di VS Code
- Nel file vuoto, scrivi solo questo: `!`
- Poi premi il tasto `Tab`
- BOOM! VS Code crea automaticamente tutta la struttura HTML per te!

### Passo 5: Modifica il contenuto
- Cambia il `<title>` in qualcosa di tuo
- Scrivi un titolo `<h1>` dentro il `<body>`
- Aggiungi un paragrafo `<p>`

### Passo 6: Salva e visualizza
- Premi `Ctrl + S` (Windows) o `Cmd + S` (Mac) per salvare
- Click destro sul file > "Open with Live Server"
- Il tuo browser si aprirà con la tua pagina!

## 🎨 Esempio Harry Potter Completo

Ecco un esempio più completo con tema Harry Potter:

```html
<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Scuola di Magia e Stregoneria di Hogwarts</title>
</head>
<body>
    <h1>Benvenuto a Hogwarts!</h1>
    <h2>La scuola di magia più famosa del mondo</h2>

    <p>
        Hogwarts è una scuola di magia e stregoneria fondata oltre mille anni fa
        dai quattro maghi più potenti dell'epoca.
    </p>

    <h3>Le Quattro Case</h3>
    <p>
        Ogni studente viene smistato in una delle quattro case:
        Grifondoro, Serpeverde, Tassorosso o Corvonero.
    </p>

    <h3>Materie Principali</h3>
    <p>
        Gli studenti imparano incantesimi, pozioni, trasfigurazione,
        difesa contro le arti oscure e molto altro!
    </p>
</body>
</html>
```

**Cosa notiamo?**
- Ci sono 3 livelli di titoli: `<h1>`, `<h2>`, `<h3>` (dal più grande al più piccolo)
- I paragrafi usano il tag `<p>`
- Tutto il contenuto visibile sta dentro `<body>`
- Il codice è indentato (spostato a destra) per essere più leggibile

## 🏆 Challenge: La Tua Lettera di Hogwarts

Ora tocca a te! Crea una pagina HTML che simula la tua lettera di accettazione a Hogwarts.

**Requisiti:**
1. Titolo principale: "Scuola di Magia e Stregoneria di Hogwarts"
2. Sottotitolo: il tuo nome
3. Un paragrafo che dice: "Caro [tuo nome], siamo lieti di informarti che sei stato accettato..."
4. Un titolo "Lista Materiale"
5. Un paragrafo con almeno 3 oggetti che devi comprare (bacchetta, libro, calderone, ecc.)

**Prova a farlo da solo prima di guardare la soluzione!**

<details>
<summary>💡 Clicca qui per vedere la soluzione</summary>

```html
<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lettera di Hogwarts</title>
</head>
<body>
    <h1>Scuola di Magia e Stregoneria di Hogwarts</h1>
    <h2>Mario Rossi</h2>

    <p>
        Caro Mario, siamo lieti di informarti che sei stato accettato
        alla Scuola di Magia e Stregoneria di Hogwarts.
        Le lezioni inizieranno il 1° settembre.
    </p>

    <h3>Lista Materiale</h3>
    <p>
        Dovrai procurarti: una bacchetta magica, un calderone di peltro,
        il libro "Storia di Hogwarts", una veste da lavoro nera,
        e un animale domestico (gufo, gatto o rospo).
    </p>

    <p>In attesa di vederti sui binari del 9¾!</p>

    <p>Cordiali saluti,<br>Minerva McGranitt</p>
</body>
</html>
```
</details>

## 💡 Tips & Tricks

### Scorciatoie VS Code
- `!` + `Tab` = Crea struttura HTML completa
- `Ctrl + S` = Salva file
- `Ctrl + /` = Commenta/decomment righe (utile per nascondere codice temporaneamente)
- `Alt + Shift + ↓` = Duplica la riga corrente

### Commenti in HTML
Puoi scrivere note nel tuo codice che il browser ignorerà:

```html
<!-- Questo è un commento. Non si vede sulla pagina! -->
<h1>Questo invece si vede</h1>
```

### Errori Comuni da Evitare
- ❌ Dimenticare di chiudere i tag: `<p>Testo` (manca `</p>`)
- ❌ Tag annidati male: `<h1><p>Testo</h1></p>` (dovrebbe essere `<h1>Testo</h1><p>Altro</p>`)
- ❌ Non salvare prima di ricaricare il browser
- ❌ Scrivere tag in maiuscolo: usa `<div>` non `<DIV>`

### Tag che si chiudono da soli
Alcuni tag non hanno bisogno di chiusura:
- `<br>` - Vai a capo
- `<img>` - Immagine (lo vedremo dopo)
- `<hr>` - Linea orizzontale
- `<meta>` - Metadati

## ✅ Checklist: Cosa hai imparato

Segna quello che hai capito:

- [ ] So cos'è HTML e a cosa serve
- [ ] Conosco la struttura base di una pagina HTML
- [ ] So creare un file `.html` in VS Code
- [ ] So usare i tag `<h1>`, `<h2>`, `<p>`
- [ ] So aprire la mia pagina con Live Server
- [ ] So usare la scorciatoia `!` + `Tab`
- [ ] Ho completato la challenge della lettera di Hogwarts

## 🎯 Prossimi Passi

Ora che conosci le basi, nella [prossima lezione](02-html-base.md) impareremo:
- Altri tag HTML importanti (liste, link, immagini)
- Come formattare il testo (grassetto, corsivo)
- Come collegare pagine diverse

**Importante:** Prima di passare alla lezione 2, assicurati di aver completato la challenge! La pratica è fondamentale.

---

*"Le parole sono, nella mia non modesta opinione, la nostra massima e inesauribile fonte di magia."* - Albus Silente

E HTML è fatto di parole... o meglio, di tag! 🪄
