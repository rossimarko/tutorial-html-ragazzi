# Esercizio 2: Liste di Incantesimi e Pozioni

## 📖 Storia / Contesto

Il Professor Vitious ti ha chiesto di creare una pagina con le liste degli incantesimi che imparerai quest'anno. La Prof.ssa Sprite vuole anche una lista delle piante da studiare in Erbologia. Usa le liste HTML per organizzare tutto!

## 🎯 Obiettivo

Imparare a creare e usare liste ordinate (`<ol>`) e non ordinate (`<ul>`), e liste annidate.

## 📋 Richieste

La tua pagina `incantesimi.html` deve contenere:

1. **Titolo principale**: "Guida agli Incantesimi - Primo Anno"
2. **Sezione Incantesimi Base** (lista non ordinata con `<ul>`):
   - Lumos (luce)
   - Nox (spegni luce)
   - Alohomora (apri)
   - Wingardium Leviosa (levitazione)
   - Expelliarmus (disarma)

3. **Sezione Passi per Lanciare un Incantesimo** (lista ordinata con `<ol>`):
   - Impugna la bacchetta correttamente
   - Pronuncia chiaramente le parole magiche
   - Visualizza l'effetto desiderato
   - Esegui il movimento della bacchetta

4. **Sezione Pozioni** (lista non ordinata):
   - Felix Felicis
   - Veritaserum
   - Pozione Calderone Fuso
   - Antidoto ai Veleni Comuni

5. **Sezione Ingredienti per Pozione Rigonfiante** (lista ordinata numerata):
   - Occhi di scarafaggio essiccati (3 pezzi)
   - Veleno di serpente (2 gocce)
   - Radice di zenzero (1 pizzico)

6. **Bonus**: Una lista annidata - Materie per anno:
   - Primo Anno
     - Pozioni
     - Incantesimi
     - Trasfigurazione
   - Secondo Anno
     - Difesa contro le Arti Oscure
     - Erbologia

## 🚀 Starter Code

```html
<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Incantesimi e Pozioni</title>
</head>
<body>
    <h1>Guida agli Incantesimi - Primo Anno</h1>

    <!-- Sezione 1: Incantesimi Base -->
    <h2>Incantesimi Base</h2>
    <ul>
        <!-- Completa qui -->
    </ul>

    <!-- Sezione 2: Passi -->
    <h2>Come Lanciare un Incantesimo</h2>
    <ol>
        <!-- Completa qui -->
    </ol>

    <!-- Continua tu... -->

</body>
</html>
```

## ✅ Output Atteso

La pagina dovrebbe mostrare:
- Liste punteate per incantesimi e pozioni
- Liste numerate per passi e ingredienti
- Liste ben formattate e leggibili
- Liste annidate con indentazione corretta

## 💡 Suggerimenti

1. `<ul>` = Unordered List (lista non ordinata, con pallini)
2. `<ol>` = Ordered List (lista ordinata, con numeri)
3. `<li>` = List Item (elemento della lista)
4. Ogni `<li>` deve essere dentro `<ul>` o `<ol>`
5. Ricorda di chiudere tutti i tag: `</li>`, `</ul>`, `</ol>`
6. Per liste annidate, metti un `<ul>` dentro un `<li>`

## ✨ Soluzione Completa

<details>
<summary>💡 Clicca qui per vedere la soluzione</summary>

```html
<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Incantesimi e Pozioni - Primo Anno</title>
</head>
<body>
    <h1>Guida agli Incantesimi - Primo Anno</h1>

    <p>Benvenuto alla guida completa degli incantesimi e pozioni che studierai quest'anno!</p>

    <hr>

    <!-- Incantesimi Base -->
    <h2>Incantesimi Base</h2>
    <p>Questi sono gli incantesimi fondamentali che ogni mago deve conoscere:</p>
    <ul>
        <li><strong>Lumos</strong> - Crea una luce dalla punta della bacchetta</li>
        <li><strong>Nox</strong> - Spegne la luce creata da Lumos</li>
        <li><strong>Alohomora</strong> - Apre porte e serrature</li>
        <li><strong>Wingardium Leviosa</strong> - Fa levitare gli oggetti</li>
        <li><strong>Expelliarmus</strong> - Disarma l'avversario</li>
    </ul>

    <hr>

    <!-- Passi per Lanciare Incantesimo -->
    <h2>Come Lanciare un Incantesimo Correttamente</h2>
    <p>Segui questi passi nell'ordine:</p>
    <ol>
        <li>Impugna la bacchetta correttamente (con fermezza ma senza stringere troppo)</li>
        <li>Pronuncia chiaramente le parole magiche</li>
        <li>Visualizza mentalmente l'effetto desiderato</li>
        <li>Esegui il movimento della bacchetta con precisione</li>
    </ol>

    <hr>

    <!-- Pozioni -->
    <h2>Pozioni Importanti</h2>
    <p>Queste pozioni saranno studiate durante l'anno:</p>
    <ul>
        <li>Felix Felicis (Pozione della Fortuna)</li>
        <li>Veritaserum (Pozione della Verità)</li>
        <li>Pozione Calderone Fuso</li>
        <li>Antidoto ai Veleni Comuni</li>
    </ul>

    <hr>

    <!-- Ricetta Pozione -->
    <h2>Ricetta: Pozione Rigonfiante</h2>
    <p>Ingredienti nell'ordine di aggiunta:</p>
    <ol>
        <li>Occhi di scarafaggio essiccati (3 pezzi)</li>
        <li>Veleno di serpente (2 gocce)</li>
        <li>Radice di zenzero tritata (1 pizzico)</li>
    </ol>

    <hr>

    <!-- Lista Annidata -->
    <h2>Materie per Anno</h2>
    <ul>
        <li>
            <strong>Primo Anno</strong>
            <ul>
                <li>Pozioni</li>
                <li>Incantesimi</li>
                <li>Trasfigurazione</li>
            </ul>
        </li>
        <li>
            <strong>Secondo Anno</strong>
            <ul>
                <li>Difesa contro le Arti Oscure</li>
                <li>Erbologia</li>
                <li>Storia della Magia</li>
            </ul>
        </li>
    </ul>

    <hr>

    <p><small>Guida compilata dal Prof. Vitious - Anno Scolastico 2024/2025</small></p>
</body>
</html>
```
</details>

## 🎨 Varianti e Sfide Bonus

### Variante 1: Lista Ingredienti Complessa
Crea una ricetta di pozione con lista annidata:
- Ingredienti principali
  - Liquidi
  - Solidi
- Ingredienti opzionali

### Variante 2: Top 5 Incantesimi
Crea una classifica ordinata (dal 5° al 1°) dei tuoi incantesimi preferiti

### Variante 3: Aggiungi Descrizioni
Usa `<strong>` per il nome dell'incantesimo e testo normale per la descrizione

## 🔍 Checklist di Verifica

- [ ] Il file si chiama `incantesimi.html`
- [ ] Ci sono almeno 2 liste non ordinate (`<ul>`)
- [ ] Ci sono almeno 2 liste ordinate (`<ol>`)
- [ ] Ogni elemento lista ha `<li>` e `</li>`
- [ ] C'è almeno una lista annidata
- [ ] Il codice è indentato correttamente
- [ ] Tutti i tag sono chiusi
- [ ] La pagina si visualizza correttamente

## 📚 Cosa Hai Imparato

- Differenza tra `<ul>` e `<ol>`
- Come usare `<li>` dentro le liste
- Come annidare liste dentro liste
- Formattare liste con `<strong>` e altri tag

## 🎯 Prossimo Passo

Fantastico! Passa al [Esercizio 3: Form di Iscrizione](es03-form.md)!

---

*"La precisione è fondamentale nelle pozioni, così come nelle liste HTML!"* - Prof. Piton 🧪
