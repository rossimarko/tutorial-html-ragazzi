# Esercizio 1: La Tua Prima Pagina HTML

## 📖 Storia / Contesto

Sei stato appena accettato a Hogwarts! Il Professor Silente ti ha chiesto di creare la tua prima pagina web personale da mostrare agli altri studenti. È il momento di mettere in pratica quello che hai imparato!

## 🎯 Obiettivo

Creare una pagina HTML di presentazione personale usando i tag base: titoli, paragrafi, link e immagini.

## 📋 Richieste

La tua pagina deve contenere:

1. **Struttura HTML completa** (DOCTYPE, html, head, body)
2. **Title** nella sezione head: "La mia pagina Hogwarts - [Tuo Nome]"
3. **Titolo principale (h1)**: Il tuo nome
4. **Sottotitolo (h2)**: "Studente di Hogwarts - Primo Anno"
5. **Paragrafo** di presentazione (3-5 righe su di te)
6. **Titolo h3**: "La mia Casa"
7. **Paragrafo** che dice in quale casa vorresti essere e perché
8. **Titolo h3**: "Le mie materie preferite"
9. **Paragrafo** che elenca 3 materie che vorresti studiare
10. **Linea orizzontale** (`<hr>`)
11. **Link** a Google (si apre in nuova scheda)
12. **Messaggio di chiusura** in un paragrafo piccolo (`<small>`)

## 🚀 Starter Code

Crea un file `mia-pagina.html` e parti da questa struttura:

```html
<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title><!-- Inserisci qui il titolo --></title>
</head>
<body>
    <!-- Il tuo codice qui -->

</body>
</html>
```

## ✅ Output Atteso

La pagina finale dovrebbe mostrare:
- Il tuo nome come titolo grande
- Informazioni su di te in paragrafi ben formattati
- La tua casa preferita
- Le materie che vuoi studiare
- Un link funzionante
- Una struttura HTML valida e ben indentata

## 💡 Suggerimenti

1. Usa `!` + `Tab` in VS Code per creare la struttura HTML base
2. Ricorda di chiudere tutti i tag
3. Indenta il codice per renderlo leggibile
4. Salva spesso con `Ctrl + S`
5. Apri con Live Server per vedere il risultato
6. Per il link che apre in nuova scheda usa `target="_blank"`

## ✨ Soluzione Completa

<details>
<summary>💡 Clicca qui per vedere una soluzione d'esempio</summary>

```html
<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>La mia pagina Hogwarts - Mario Rossi</title>
</head>
<body>
    <h1>Mario Rossi</h1>
    <h2>Studente di Hogwarts - Primo Anno</h2>

    <p>
        Ciao! Mi chiamo Mario e ho 12 anni. Sono appena stato accettato
        a Hogwarts e non vedo l'ora di iniziare questa avventura magica.
        Amo leggere libri di incantesimi e sperimentare con le pozioni.
        Il mio sogno è diventare un grande mago come Albus Silente!
    </p>

    <h3>La mia Casa</h3>
    <p>
        Vorrei essere smistato in <strong>Grifondoro</strong> perché
        mi identifico con i valori di coraggio e lealtà. Ammiro molto
        Harry Potter e i suoi amici, e spero di poter vivere avventure
        simili alle loro!
    </p>

    <h3>Le mie materie preferite</h3>
    <p>
        Non vedo l'ora di studiare <strong>Pozioni</strong> con il Professor Piton
        (anche se dicono sia severo!), <strong>Difesa contro le Arti Oscure</strong>
        perché voglio imparare a proteggermi, e <strong>Trasfigurazione</strong>
        perché trasformare gli oggetti mi sembra magico!
    </p>

    <hr>

    <p>
        Per saperne di più sulla magia, visita
        <a href="https://www.google.com/search?q=harry+potter+hogwarts" target="_blank">
            Google
        </a>
    </p>

    <p>
        <small>Questa pagina è stata creata da Mario Rossi - Anno Scolastico 2024/2025</small>
    </p>
</body>
</html>
```
</details>

## 🎨 Varianti e Sfide Bonus

Una volta completato l'esercizio base, prova queste varianti:

### Variante 1: Aggiungi Formattazione
- Usa `<em>` per mettere in corsivo alcune parole
- Usa `<strong>` per enfatizzare concetti importanti
- Usa `<mark>` per evidenziare qualcosa

### Variante 2: Aggiungi più Sezioni
- Sezione "I miei amici" con nomi di compagni
- Sezione "I miei obiettivi" con lista di cose che vuoi imparare
- Sezione "Contatti" con un link email (`mailto:`)

### Variante 3: Personalizza
- Cambia tutti i riferimenti con informazioni vere su di te
- Aggiungi una sezione sui tuoi hobby reali
- Inserisci più link a siti che ti piacciono

## 🔍 Checklist di Verifica

Prima di considerare l'esercizio completato, verifica:

- [ ] Il file si chiama `mia-pagina.html`
- [ ] La struttura HTML è completa (DOCTYPE, html, head, body)
- [ ] Il title è personalizzato
- [ ] Ci sono almeno 3 livelli di titoli (h1, h2, h3)
- [ ] Ci sono almeno 4 paragrafi
- [ ] C'è una linea orizzontale `<hr>`
- [ ] C'è un link funzionante che si apre in nuova scheda
- [ ] Il codice è indentato correttamente
- [ ] Non ci sono errori (controlla la console del browser con F12)
- [ ] La pagina si apre correttamente con Live Server

## 📚 Cosa Hai Imparato

Completando questo esercizio hai praticato:
- La struttura base di una pagina HTML
- Titoli gerarchici (h1, h2, h3)
- Paragrafi
- Formattazione testo (strong, em, small)
- Link esterni
- Organizzazione del codice

## 🎯 Prossimo Passo

Ottimo lavoro! Passa al [Esercizio 2: Liste](es02-liste.md) per imparare a creare liste ordinate e non ordinate!

---

*"Ogni grande mago è stato un principiante. Non aver paura di sbagliare!"* 🪄
