# Esercizio 3: Modulo di Iscrizione a Hogwarts

## 📖 Storia / Contesto

Il Ministero della Magia ha deciso di digitalizzare le iscrizioni a Hogwarts! Ti hanno incaricato di creare il modulo di iscrizione online. Gli studenti dovranno compilare tutte le informazioni necessarie prima di ricevere la lettera ufficiale.

## 🎯 Obiettivo

Creare un form HTML completo con tutti i tipi di input: text, email, date, radio, checkbox, select, textarea e button.

## 📋 Richieste

Crea `iscrizione-hogwarts.html` con un form che include:

1. **Dati Personali**:
   - Nome completo (input text, obbligatorio)
   - Email (input email, obbligatorio)
   - Data di nascita (input date)
   - Età (input number, min=11, max=17)

2. **Preferenza Casa** (radio button - scelta singola):
   - Grifondoro
   - Serpeverde
   - Tassorosso
   - Corvonero

3. **Materie di Interesse** (checkbox - scelta multipla):
   - Pozioni
   - Incantesimi
   - Trasfigurazione
   - Difesa contro le Arti Oscure
   - Volo

4. **Anno di Corso** (select dropdown):
   - Primo Anno
   - Secondo Anno
   - Terzo Anno
   - Quarto Anno
   - Quinto Anno

5. **Motivazione** (textarea):
   - "Perché vuoi frequentare Hogwarts?" (5 righe)

6. **Tipo di Bacchetta Preferita** (select):
   - Legno di Agrifoglio
   - Legno di Vite
   - Legno di Sambuco
   - Legno di Frassino

7. **Accettazione Privacy** (checkbox obbligatorio)

8. **Pulsanti**:
   - Invia Candidatura (submit)
   - Cancella Tutto (reset)

## 🚀 Starter Code

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
    <p>Compila tutti i campi per richiedere l'ammissione</p>

    <hr>

    <form>
        <h2>Dati Personali</h2>

        <label for="nome">Nome completo:</label><br>
        <input type="text" id="nome" name="nome" required><br><br>

        <!-- Continua tu... -->

    </form>
</body>
</html>
```

## ✅ Output Atteso

Il form finale dovrebbe:
- Essere completo e funzionante
- Avere tutti i campi con label appropriate
- Validare i campi obbligatori
- Permettere di scegliere una sola casa (radio)
- Permettere di scegliere più materie (checkbox)
- Avere menu dropdown funzionanti
- Avere textarea per testo lungo
- Avere pulsanti submit e reset

## 💡 Suggerimenti

1. Usa sempre `<label for="id">` collegato a `id="id"` dell'input
2. Aggiungi `required` ai campi obbligatori
3. I radio button dello stesso gruppo devono avere lo stesso `name`
4. Usa `<br><br>` per spaziare i campi
5. Dividi in sezioni con `<h2>` e `<hr>`
6. Usa `placeholder` per dare esempi all'utente

## ✨ Soluzione Completa

<details>
<summary>💡 Clicca qui per vedere la soluzione</summary>

```html
<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Iscrizione a Hogwarts</title>
</head>
<body>
    <h1>🏰 Modulo di Iscrizione a Hogwarts</h1>
    <p>Benvenuto! Compila il modulo per richiedere l'ammissione alla Scuola di Magia e Stregoneria di Hogwarts.</p>

    <hr>

    <form>
        <!-- SEZIONE DATI PERSONALI -->
        <h2>📋 Dati Personali</h2>

        <label for="nome">Nome completo:</label><br>
        <input type="text" id="nome" name="nome" placeholder="Harry Potter" required><br><br>

        <label for="email">Email:</label><br>
        <input type="email" id="email" name="email" placeholder="harry@hogwarts.com" required><br><br>

        <label for="nascita">Data di nascita:</label><br>
        <input type="date" id="nascita" name="nascita"><br><br>

        <label for="eta">Età:</label><br>
        <input type="number" id="eta" name="eta" min="11" max="17" placeholder="11"><br><br>

        <hr>

        <!-- SEZIONE CASA -->
        <h2>🏠 Preferenza Casa</h2>
        <p>In quale casa vorresti essere smistato?</p>

        <input type="radio" id="grifondoro" name="casa" value="grifondoro">
        <label for="grifondoro">🦁 Grifondoro (Coraggio e audacia)</label><br>

        <input type="radio" id="serpeverde" name="casa" value="serpeverde">
        <label for="serpeverde">🐍 Serpeverde (Astuzia e ambizione)</label><br>

        <input type="radio" id="tassorosso" name="casa" value="tassorosso">
        <label for="tassorosso">🦡 Tassorosso (Lealtà e pazienza)</label><br>

        <input type="radio" id="corvonero" name="casa" value="corvonero">
        <label for="corvonero">🦅 Corvonero (Intelligenza e creatività)</label><br><br>

        <hr>

        <!-- SEZIONE MATERIE -->
        <h2>📚 Materie di Interesse</h2>
        <p>Seleziona le materie che ti interessano di più (puoi sceglierne più di una):</p>

        <input type="checkbox" id="pozioni" name="materie" value="pozioni">
        <label for="pozioni">Pozioni</label><br>

        <input type="checkbox" id="incantesimi" name="materie" value="incantesimi">
        <label for="incantesimi">Incantesimi</label><br>

        <input type="checkbox" id="trasfigurazione" name="materie" value="trasfigurazione">
        <label for="trasfigurazione">Trasfigurazione</label><br>

        <input type="checkbox" id="difesa" name="materie" value="difesa">
        <label for="difesa">Difesa contro le Arti Oscure</label><br>

        <input type="checkbox" id="volo" name="materie" value="volo">
        <label for="volo">Volo</label><br><br>

        <hr>

        <!-- SEZIONE ANNO -->
        <h2>📅 Anno di Corso</h2>

        <label for="anno">Seleziona l'anno:</label>
        <select id="anno" name="anno" required>
            <option value="">-- Scegli un anno --</option>
            <option value="1">Primo Anno</option>
            <option value="2">Secondo Anno</option>
            <option value="3">Terzo Anno</option>
            <option value="4">Quarto Anno</option>
            <option value="5">Quinto Anno</option>
        </select><br><br>

        <hr>

        <!-- SEZIONE BACCHETTA -->
        <h2>🪄 Tipo di Bacchetta Preferita</h2>

        <label for="bacchetta">Scegli il tipo di legno:</label>
        <select id="bacchetta" name="bacchetta">
            <option value="">-- Scegli --</option>
            <option value="agrifoglio">Legno di Agrifoglio (come Harry)</option>
            <option value="vite">Legno di Vite (come Hermione)</option>
            <option value="sambuco">Legno di Sambuco (come Silente)</option>
            <option value="frassino">Legno di Frassino (come Ron)</option>
        </select><br><br>

        <hr>

        <!-- SEZIONE MOTIVAZIONE -->
        <h2>✍️ Motivazione</h2>

        <label for="motivazione">Perché vuoi frequentare Hogwarts?</label><br>
        <textarea id="motivazione" name="motivazione" rows="5" cols="50"
                  placeholder="Scrivi qui le tue motivazioni..."></textarea><br><br>

        <hr>

        <!-- PRIVACY -->
        <h2>🔒 Privacy</h2>

        <input type="checkbox" id="privacy" name="privacy" required>
        <label for="privacy">
            Accetto che i miei dati siano utilizzati dal Ministero della Magia
            per finalità didattiche
        </label><br><br>

        <hr>

        <!-- PULSANTI -->
        <button type="submit">📨 Invia Candidatura</button>
        <button type="reset">🗑️ Cancella Tutto</button>

    </form>

    <hr>

    <p><small>Modulo creato dal Ministero della Magia - Dipartimento Educazione Magica</small></p>
</body>
</html>
```
</details>

## 🎨 Varianti e Sfide Bonus

### Variante 1: Aggiungi Fieldset
Usa `<fieldset>` e `<legend>` per raggruppare sezioni correlate

```html
<fieldset>
    <legend>Dati Personali</legend>
    <!-- Campi qui -->
</fieldset>
```

### Variante 2: Aggiungi Range Input
Aggiungi un campo per "Livello di esperienza in magia" (0-10) con `<input type="range">`

### Variante 3: Aggiungi Upload File
Aggiungi campo per caricare la foto (`<input type="file">`)

### Variante 4: Aggiungi Validazione Pattern
Usa `pattern` per validare formati specifici (es: codice studente)

## 🔍 Checklist di Verifica

- [ ] Il file si chiama `iscrizione-hogwarts.html`
- [ ] Form completo con tag `<form>`
- [ ] Tutti i campi hanno `<label>` collegata
- [ ] Ci sono input: text, email, date, number
- [ ] Ci sono radio button per scelta singola
- [ ] Ci sono checkbox per scelta multipla
- [ ] Ci sono 2 select dropdown
- [ ] C'è una textarea
- [ ] Ci sono pulsanti submit e reset
- [ ] Campi obbligatori hanno `required`
- [ ] Il codice è ben indentato

## 📚 Cosa Hai Imparato

- Creare form completi con `<form>`
- Usare tutti i tipi di input principali
- Collegare label agli input
- Validazione base con `required`, `min`, `max`
- Radio button vs checkbox
- Select per menu dropdown
- Textarea per testi lunghi
- Pulsanti submit e reset

## 🎯 Prossimo Passo

Eccellente! Passa al [Esercizio 4: Layout Grid](es04-grid.md) per imparare Bootstrap Grid!

---

*"Compilare form è come preparare una pozione: ogni ingrediente (campo) è importante!"* 🧪📝
