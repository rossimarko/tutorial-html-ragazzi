# Lezione 3: HTML Form - Moduli Interattivi

Benvenuto alla terza lezione! Oggi imparerai a creare form (moduli) che permettono agli utenti di inserire dati. È come creare il modulo di iscrizione a Hogwarts!

## 🎯 Obiettivi della Lezione

Alla fine di questa lezione saprai:
- Creare form con il tag `<form>`
- Usare input di testo, email, password
- Creare checkbox, radio button, e select
- Aggiungere pulsanti di invio
- Strutturare form accessibili e user-friendly

## 🧙 Concetti Fondamentali

### Cosa sono i Form?

Un **form** (modulo) è una sezione della pagina dove gli utenti possono **inserire dati**: nome, email, password, scelte, ecc.

Esempi di form che usi tutti i giorni:
- Login a Instagram/TikTok → Username e password
- Iscrizione a un sito → Nome, email, data di nascita
- Sondaggio online → Domande con scelte multiple
- Motore di ricerca Google → Campo di ricerca

### Struttura Base

Tutti i form iniziano con il tag `<form>`:

```html
<form>
    <!-- Qui dentro vanno tutti i campi del form -->
</form>
```

## ⚡ Analogia Harry Potter

Pensa ai form HTML come al **Registro di Hogwarts**:

- `<form>` = Il modulo completo di iscrizione
- `<input type="text">` = Campo dove scrivi il nome con la penna magica
- `<input type="checkbox">` = Caselle da spuntare per scegliere le materie
- `<select>` = Il Cappello Parlante che ti fa scegliere tra le Case
- `<button>` = Il sigillo magico che invia il modulo

Quando completi un form e clicchi "Invia", è come quando la tua lettera di Hogwarts viene inviata tramite civetta!

## 💻 Input di Testo

### Input Testo Semplice
```html
<label for="nome">Nome:</label>
<input type="text" id="nome" name="nome" placeholder="Inserisci il tuo nome">
```

**Parti importanti:**
- `<label>` = Etichetta che descrive il campo
- `for="nome"` = Collega la label all'input
- `type="text"` = Campo di testo normale
- `id="nome"` = Identificatore unico (deve corrispondere al `for`)
- `name="nome"` = Nome del campo quando invii i dati
- `placeholder` = Testo di esempio che scompare quando scrivi

### Input Email
```html
<label for="email">Email:</label>
<input type="email" id="email" name="email" placeholder="tua@email.com" required>
```
Il browser controlla automaticamente che sia un'email valida!

### Input Password
```html
<label for="password">Password:</label>
<input type="password" id="password" name="password" required>
```
I caratteri vengono nascosti con pallini •••

### Input Numero
```html
<label for="eta">Età:</label>
<input type="number" id="eta" name="eta" min="11" max="17">
```

### Input Data
```html
<label for="nascita">Data di nascita:</label>
<input type="date" id="nascita" name="nascita">
```

## ☑️ Checkbox e Radio Button

### Checkbox (Caselle multiple)
Permettono di scegliere **più opzioni contemporaneamente**:

```html
<p>Seleziona le materie che vuoi studiare:</p>

<input type="checkbox" id="pozioni" name="materie" value="pozioni">
<label for="pozioni">Pozioni</label><br>

<input type="checkbox" id="incantesimi" name="materie" value="incantesimi">
<label for="incantesimi">Incantesimi</label><br>

<input type="checkbox" id="trasfigurazione" name="materie" value="trasfigurazione">
<label for="trasfigurazione">Trasfigurazione</label>
```

### Radio Button (Scelta singola)
Permettono di scegliere **solo una opzione** tra tante:

```html
<p>Seleziona la tua casa preferita:</p>

<input type="radio" id="grifondoro" name="casa" value="grifondoro">
<label for="grifondoro">Grifondoro</label><br>

<input type="radio" id="serpeverde" name="casa" value="serpeverde">
<label for="serpeverde">Serpeverde</label><br>

<input type="radio" id="tassorosso" name="casa" value="tassorosso">
<label for="tassorosso">Tassorosso</label><br>

<input type="radio" id="corvonero" name="casa" value="corvonero">
<label for="corvonero">Corvonero</label>
```

**Importante:** Tutti i radio button dello stesso gruppo devono avere lo stesso `name`!

## 📋 Select - Menu a Tendina

Per creare un menu dropdown:

```html
<label for="anno">Seleziona l'anno:</label>
<select id="anno" name="anno">
    <option value="">-- Scegli --</option>
    <option value="1">Primo Anno</option>
    <option value="2">Secondo Anno</option>
    <option value="3">Terzo Anno</option>
    <option value="4">Quarto Anno</option>
    <option value="5">Quinto Anno</option>
</select>
```

## 📝 Textarea - Testo Lungo

Per testi più lunghi (es: commenti, messaggi):

```html
<label for="messaggio">Scrivi un messaggio:</label><br>
<textarea id="messaggio" name="messaggio" rows="5" cols="40" placeholder="Scrivi qui..."></textarea>
```

## 🔘 Button - Pulsanti

### Pulsante di invio
```html
<button type="submit">Invia Modulo</button>
```

### Pulsante normale
```html
<button type="button">Clicca qui</button>
```

### Pulsante reset (cancella tutto)
```html
<button type="reset">Cancella tutto</button>
```

## 🎨 Esempio Harry Potter Completo

Ecco un form completo di iscrizione a Hogwarts:

```html
<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Iscrizione Hogwarts</title>
</head>
<body>
    <h1>Modulo di Iscrizione a Hogwarts</h1>
    <p>Compila il modulo per richiedere l'ammissione alla scuola di magia</p>

    <hr>

    <form>
        <!-- Dati Personali -->
        <h2>Dati Personali</h2>

        <label for="nome">Nome completo:</label><br>
        <input type="text" id="nome" name="nome" placeholder="Harry Potter" required><br><br>

        <label for="email">Email:</label><br>
        <input type="email" id="email" name="email" placeholder="harry@hogwarts.com" required><br><br>

        <label for="eta">Età:</label><br>
        <input type="number" id="eta" name="eta" min="11" max="17" required><br><br>

        <label for="nascita">Data di nascita:</label><br>
        <input type="date" id="nascita" name="nascita"><br><br>

        <hr>

        <!-- Scelta Casa -->
        <h2>Preferenze Casa</h2>
        <p>In quale casa vorresti essere smistato?</p>

        <input type="radio" id="grifondoro" name="casa" value="grifondoro">
        <label for="grifondoro">🦁 Grifondoro (Coraggio)</label><br>

        <input type="radio" id="serpeverde" name="casa" value="serpeverde">
        <label for="serpeverde">🐍 Serpeverde (Astuzia)</label><br>

        <input type="radio" id="tassorosso" name="casa" value="tassorosso">
        <label for="tassorosso">🦡 Tassorosso (Lealtà)</label><br>

        <input type="radio" id="corvonero" name="casa" value="corvonero">
        <label for="corvonero">🦅 Corvonero (Intelligenza)</label><br><br>

        <hr>

        <!-- Materie -->
        <h2>Materie di Interesse</h2>
        <p>Seleziona le materie che ti interessano di più:</p>

        <input type="checkbox" id="pozioni" name="materie" value="pozioni">
        <label for="pozioni">Pozioni</label><br>

        <input type="checkbox" id="incantesimi" name="materie" value="incantesimi">
        <label for="incantesimi">Incantesimi</label><br>

        <input type="checkbox" id="trasfigurazione" name="materie" value="trasfigurazione">
        <label for="trasfigurazione">Trasfigurazione</label><br>

        <input type="checkbox" id="difesa" name="materie" value="difesa">
        <label for="difesa">Difesa contro le Arti Oscure</label><br>

        <input type="checkbox" id="erbologia" name="materie" value="erbologia">
        <label for="erbologia">Erbologia</label><br><br>

        <hr>

        <!-- Anno -->
        <h2>Anno di Corso</h2>

        <label for="anno">Seleziona anno:</label>
        <select id="anno" name="anno" required>
            <option value="">-- Scegli un anno --</option>
            <option value="1">Primo Anno</option>
            <option value="2">Secondo Anno</option>
            <option value="3">Terzo Anno</option>
            <option value="4">Quarto Anno</option>
            <option value="5">Quinto Anno</option>
            <option value="6">Sesto Anno</option>
            <option value="7">Settimo Anno</option>
        </select><br><br>

        <hr>

        <!-- Messaggio -->
        <h2>Perché vuoi frequentare Hogwarts?</h2>

        <textarea id="motivazione" name="motivazione" rows="5" cols="50"
                  placeholder="Scrivi qui le tue motivazioni..."></textarea><br><br>

        <hr>

        <!-- Privacy -->
        <input type="checkbox" id="privacy" name="privacy" required>
        <label for="privacy">Accetto che i miei dati siano usati dal Ministero della Magia</label><br><br>

        <!-- Pulsanti -->
        <button type="submit">🪄 Invia Candidatura</button>
        <button type="reset">❌ Cancella tutto</button>
    </form>

    <hr>

    <p><small>Per informazioni contatta l'ufficio ammissioni di Hogwarts</small></p>
</body>
</html>
```

## 🛠️ Attributi Utili

### required
Rende il campo obbligatorio:
```html
<input type="text" name="nome" required>
```

### placeholder
Testo di esempio nel campo:
```html
<input type="text" placeholder="Inserisci qui...">
```

### minlength e maxlength
Lunghezza minima e massima:
```html
<input type="text" minlength="3" maxlength="20">
```

### min e max
Per numeri:
```html
<input type="number" min="0" max="100">
```

### disabled
Disabilita il campo:
```html
<input type="text" value="Non modificabile" disabled>
```

### readonly
Solo lettura (non modificabile ma inviabile):
```html
<input type="text" value="Solo lettura" readonly>
```

### checked
Pre-seleziona checkbox o radio:
```html
<input type="checkbox" checked>
<input type="radio" name="casa" value="grifondoro" checked>
```

## 🏆 Challenge: Quiz Hogwarts

Crea un quiz interattivo su Harry Potter con un form!

**Requisiti:**
1. Titolo "Quiz Hogwarts"
2. Campo nome (obbligatorio)
3. 3 domande a risposta multipla con radio button:
   - "Chi è il preside di Hogwarts?" (3 opzioni)
   - "Quante case ci sono?" (3 opzioni)
   - "Qual è la materia di Piton?" (3 opzioni)
4. Una domanda con checkbox: "Quali di questi sono personaggi?" (4 opzioni, multiple)
5. Un menu a tendina con "Quanto conosci Harry Potter?" (Poco, Abbastanza, Molto, Esperto)
6. Textarea per "Scrivi la tua scena preferita"
7. Checkbox privacy (obbligatorio)
8. Pulsante "Invia Quiz"

<details>
<summary>💡 Clicca qui per vedere una soluzione</summary>

```html
<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Quiz Hogwarts</title>
</head>
<body>
    <h1>🧙‍♂️ Quiz su Harry Potter</h1>
    <p>Metti alla prova la tua conoscenza del mondo magico!</p>

    <hr>

    <form>
        <label for="nome">Il tuo nome:</label><br>
        <input type="text" id="nome" name="nome" required><br><br>

        <hr>

        <!-- Domanda 1 -->
        <h3>1. Chi è il preside di Hogwarts?</h3>
        <input type="radio" id="d1a" name="domanda1" value="silente">
        <label for="d1a">Albus Silente</label><br>

        <input type="radio" id="d1b" name="domanda1" value="piton">
        <label for="d1b">Severus Piton</label><br>

        <input type="radio" id="d1c" name="domanda1" value="mcgranitt">
        <label for="d1c">Minerva McGranitt</label><br><br>

        <!-- Domanda 2 -->
        <h3>2. Quante case ci sono a Hogwarts?</h3>
        <input type="radio" id="d2a" name="domanda2" value="3">
        <label for="d2a">3</label><br>

        <input type="radio" id="d2b" name="domanda2" value="4">
        <label for="d2b">4</label><br>

        <input type="radio" id="d2c" name="domanda2" value="5">
        <label for="d2c">5</label><br><br>

        <!-- Domanda 3 -->
        <h3>3. Qual è la materia del Professor Piton?</h3>
        <input type="radio" id="d3a" name="domanda3" value="pozioni">
        <label for="d3a">Pozioni</label><br>

        <input type="radio" id="d3b" name="domanda3" value="trasfigurazione">
        <label for="d3b">Trasfigurazione</label><br>

        <input type="radio" id="d3c" name="domanda3" value="erbologia">
        <label for="d3c">Erbologia</label><br><br>

        <hr>

        <!-- Domanda 4 - Checkbox -->
        <h3>4. Quali di questi sono personaggi di Harry Potter?</h3>
        <input type="checkbox" id="p1" name="personaggi" value="harry">
        <label for="p1">Harry Potter</label><br>

        <input type="checkbox" id="p2" name="personaggi" value="frodo">
        <label for="p2">Frodo Baggins</label><br>

        <input type="checkbox" id="p3" name="personaggi" value="hermione">
        <label for="p3">Hermione Granger</label><br>

        <input type="checkbox" id="p4" name="personaggi" value="luke">
        <label for="p4">Luke Skywalker</label><br><br>

        <hr>

        <!-- Select -->
        <h3>Quanto conosci Harry Potter?</h3>
        <select id="livello" name="livello">
            <option value="">-- Seleziona --</option>
            <option value="poco">Poco</option>
            <option value="abbastanza">Abbastanza</option>
            <option value="molto">Molto</option>
            <option value="esperto">Sono un esperto!</option>
        </select><br><br>

        <hr>

        <!-- Textarea -->
        <h3>Qual è la tua scena preferita?</h3>
        <textarea name="scena" rows="4" cols="50"
                  placeholder="Descrivi la tua scena preferita..."></textarea><br><br>

        <hr>

        <!-- Privacy -->
        <input type="checkbox" id="privacy" name="privacy" required>
        <label for="privacy">Accetto la privacy policy di Hogwarts</label><br><br>

        <!-- Submit -->
        <button type="submit">📨 Invia Quiz</button>
    </form>
</body>
</html>
```
</details>

## 💡 Tips & Tricks

### Organizzare i Form con Fieldset

Per raggruppare campi correlati:

```html
<form>
    <fieldset>
        <legend>Dati Personali</legend>
        <label for="nome">Nome:</label>
        <input type="text" id="nome"><br>
        <label for="email">Email:</label>
        <input type="email" id="email">
    </fieldset>

    <fieldset>
        <legend>Preferenze</legend>
        <input type="checkbox" id="newsletter">
        <label for="newsletter">Voglio ricevere la newsletter</label>
    </fieldset>
</form>
```

### Accessibilità

Usa sempre `<label>` con gli input per rendere il form accessibile:

```html
<!-- BUONO: Label collegata -->
<label for="email">Email:</label>
<input type="email" id="email" name="email">

<!-- BUONO: Label che avvolge -->
<label>
    Email:
    <input type="email" name="email">
</label>

<!-- CATTIVO: No label -->
<input type="email" name="email">
```

### Validazione HTML5

Il browser controlla automaticamente alcuni campi:

```html
<!-- Email valida -->
<input type="email" required>

<!-- Numero tra 1 e 100 -->
<input type="number" min="1" max="100" required>

<!-- URL valido -->
<input type="url" required>

<!-- Pattern personalizzato (solo lettere) -->
<input type="text" pattern="[A-Za-z]+" title="Solo lettere">
```

## 🐛 Errori Comuni

### ❌ Errore 1: Dimenticare il name
```html
<!-- SBAGLIATO - manca name -->
<input type="text" id="nome">

<!-- GIUSTO -->
<input type="text" id="nome" name="nome">
```

### ❌ Errore 2: Radio button con name diversi
```html
<!-- SBAGLIATO - non puoi selezionarne solo uno -->
<input type="radio" id="opt1" name="scelta1" value="a">
<input type="radio" id="opt2" name="scelta2" value="b">

<!-- GIUSTO - stesso name -->
<input type="radio" id="opt1" name="scelta" value="a">
<input type="radio" id="opt2" name="scelta" value="b">
```

### ❌ Errore 3: Label senza for
```html
<!-- SBAGLIATO - label non funziona -->
<label>Nome:</label>
<input type="text" id="nome">

<!-- GIUSTO -->
<label for="nome">Nome:</label>
<input type="text" id="nome">
```

## ✅ Checklist: Cosa hai imparato

- [ ] So creare un form con `<form>`
- [ ] So usare input di tipo text, email, password, number, date
- [ ] So creare checkbox per scelte multiple
- [ ] So creare radio button per scelta singola
- [ ] So usare `<select>` per menu a tendina
- [ ] So usare `<textarea>` per testi lunghi
- [ ] So collegare `<label>` agli input con `for` e `id`
- [ ] Conosco gli attributi `required`, `placeholder`, `min`, `max`
- [ ] Ho completato il challenge del Quiz Hogwarts

## 📚 Riepilogo Tag Form

| Tag/Type | Cosa fa | Esempio |
|----------|---------|---------|
| `<form>` | Contenitore form | `<form>...</form>` |
| `<label>` | Etichetta campo | `<label for="nome">Nome</label>` |
| `<input type="text">` | Campo testo | Nome, cognome |
| `<input type="email">` | Campo email | Email valida |
| `<input type="password">` | Campo password | Password nascosta |
| `<input type="number">` | Campo numerico | Età, quantità |
| `<input type="date">` | Selettore data | Data di nascita |
| `<input type="checkbox">` | Casella multipla | Scelte multiple |
| `<input type="radio">` | Scelta singola | Una opzione |
| `<select>` | Menu a tendina | Lista opzioni |
| `<textarea>` | Testo lungo | Messaggi, commenti |
| `<button>` | Pulsante | Invia, cancella |

## 🎯 Prossimi Passi

Ottimo lavoro! Ora sai creare form interattivi completi!

Nella [prossima lezione](04-bootstrap-setup.md) inizieremo con **Bootstrap 5**: un framework che renderà i tuoi siti bellissimi senza scrivere CSS!

Prima di proseguire:
1. Completa il challenge del Quiz
2. Prova a creare un form per ordinare oggetti magici
3. Sperimenta con tutti i tipi di input

---

*"Sono le nostre scelte, Harry, che dimostrano chi siamo veramente."* - Albus Silente

E tu hai scelto di imparare i form HTML! Fantastico! 🎉
