# 🔧 LipariBank Day 1 — Fix Mission

Benvenuto nel progetto **LipariBank**! Questo è il frontend di una banca digitale immaginaria.
Il codice contiene **3 bug intenzionali** che compromettono l'esperienza utente. Il tuo compito è trovarli e risolverli.

---

## Come avviare

1. **Installa le dipendenze**
   ```bash
   npm install
   ```

2. **Compila gli stili SCSS** (in modalità watch, si ricompila ad ogni modifica)
   ```bash
   npm run dev
   ```

3. **Apri il progetto nel browser**
   Usa l'estensione **Live Server** di VS Code: tasto destro su `index.html` → *Open with Live Server*.

   > Oppure avvia manualmente `dashboard.html` nel browser.

---

## Le 3 Missioni

### Missione 1 — La pagina delle transazioni è strana sul mobile

Apri `transactions.html` su un dispositivo mobile (o usa il DevTools del browser in modalità responsive).
Noterai che la pagina **non si adatta allo schermo**: il testo è minuscolo, il layout è zoomato fuori e bisogna scrollare orizzontalmente per leggere il contenuto.
Confronta con `dashboard.html` che invece funziona correttamente su mobile.

---

### Missione 2 — Le card traboccano dalla loro colonna

Guarda la pagina `dashboard.html` con attenzione: le **card statistiche** (Saldo, Entrate, Uscite, Risparmio) dovrebbero stare ognuna nella propria colonna.
Invece sembrano allargarsi oltre il loro spazio, causando un **overflow orizzontale** della pagina.
Il problema non è nell'HTML, ma nel modo in cui il browser calcola la larghezza degli elementi.

---

### Missione 3 — La navigazione non indica la pagina corrente

Naviga dalla Dashboard alla pagina **"Il Mio Conto"** (`account.html`).
Guardando la sidebar a sinistra, dovresti vedere evidenziato il link della pagina in cui ti trovi.
Ma qualcosa non va: il link evidenziato è quello **sbagliato**.
L'utente non capisce dove si trova nell'applicazione.

---

## Struttura del progetto

```
liparibank-day1-broken/
├── index.html           → redirect automatico a dashboard.html
├── login.html           → pagina di accesso
├── dashboard.html       → panoramica conto
├── transactions.html    → storico transazioni
├── account.html         → dettagli conto
├── policy-form.html     → richiesta polizza
├── assets/
│   └── logo.svg
├── scss/
│   ├── _variables.scss  → variabili colori, font, spaziatura
│   ├── _mixins.scss     → mixin riutilizzabili
│   ├── _layout.scss     → layout globale
│   ├── _components.scss → componenti UI
│   └── main.scss        → entry point SCSS
├── dist/
│   └── main.css         → CSS compilato
└── package.json
```

Buona fortuna! 🚀
