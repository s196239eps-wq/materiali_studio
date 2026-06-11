# MatRef — Materials Engineering Academy

> Guida interattiva ai materiali da officina per ingegneri meccanici e aerospaziali

🔗 **Live demo:** `https://<tuo-username>.github.io/matref`

---

## Caratteristiche

- **22 materiali** coperti in profondità: acciai, superleghe Ni/Co, titanio, alluminio, ceramici, ghise, rame, magnesio, polimeri tecnici
- **Classifica durezza Vickers** dal diamante (10.000 HV) al PEEK (25 HV)
- **Scheda tecnica completa** per ogni materiale:
  - Struttura cristallina e chimica (fasi, legami, composizione)
  - Proprietà meccaniche (UTS, YS, E, HV, Kic, allungamento)
  - Proprietà fisiche (densità, cond. termica, T fusione)
  - Lavorabilità con indice grafico e parametri di taglio reali
  - Scorrimento viscoso / Creep
  - Saldabilità e processi di giunzione
  - Applicazioni industriali
- **Quiz AI** generato dinamicamente da Claude (10 domande per sessione, sempre diverse)
- **Responsive** — funziona su desktop, tablet, iOS e Android
- **PWA** — installabile come app su mobile

---

## Materiali inclusi

| Famiglia | Materiali |
|---|---|
| Ceramici/Abrasivi | Diamante, CBN/PCBN, SiC, WC-Co (Metallo Duro) |
| Superleghe Ni | Inconel 718, Haynes 282, MAR-M 247 (DS/SX) |
| Titanio | Ti-6Al-4V, Ti cp (Gr.1-4) |
| Acciai | H13 (hot work), 42CrMo4 (4140) |
| Acciai Inossidabili | AISI 304, AISI 316/316L, Duplex 2205 |
| Alluminio | 7075-T6, 2024-T3, 6061-T6 |
| Ghise | GG25 (grafite lamellare) |
| Rame e Leghe | Rame puro / Ottone |
| Polimeri Tecnici | PEEK |
| Magnesio | AZ31 |
| Superleghe Co | Stellite 6 |

---

## Pubblicazione su GitHub Pages

### 1. Crea il repository

```bash
# Crea un nuovo repository su github.com chiamato "matref"
# poi clona in locale:
git clone https://github.com/<tuo-username>/matref.git
cd matref
```

### 2. Copia i file

```bash
# Copia tutti i file in questa cartella nel repository clonato
cp index.html manifest.json icon.svg README.md /path/to/matref/
```

### 3. Push e attiva GitHub Pages

```bash
git add .
git commit -m "Initial deploy — MatRef Materials Academy"
git push origin main
```

Poi su GitHub:
- **Settings → Pages → Source: Deploy from a branch**
- **Branch: main / root**
- Salva — la pagina sarà disponibile in ~60 secondi

### 4. URL finale

```
https://<tuo-username>.github.io/matref/
```

---

## Quiz AI — Configurazione

Il quiz usa l'API di Anthropic (Claude). È già configurato per funzionare in produzione tramite il dominio `claude.ai` (cross-origin). Se stai facendo girare l'app da un tuo server o da GitHub Pages, potrebbe essere necessario aggiungere il tuo dominio alla lista di origini autorizzate nel tuo account Anthropic.

**Fallback:** Se l'API non è raggiungibile, il quiz usa automaticamente 5 domande statiche predefinite per il materiale selezionato.

---

## Struttura file

```
matref/
├── index.html        # App completa (single-file)
├── manifest.json     # PWA manifest
├── icon.svg          # Icona app
├── icon-192.png      # Icona PWA 192×192 (da generare)
├── icon-512.png      # Icona PWA 512×512 (da generare)
└── README.md         # Questo file
```

> **Nota:** `icon-192.png` e `icon-512.png` sono opzionali per GitHub Pages ma richiesti per l'installazione PWA su Android. Puoi generarli dal file `icon.svg` con qualsiasi editor grafico o con Inkscape.

---

## Tecnologie

- HTML5 + CSS3 + JavaScript vanilla (zero dipendenze)
- Font: IBM Plex Mono + Barlow + Barlow Condensed (Google Fonts)
- AI: Anthropic Claude API (`claude-sonnet-4-20250514`)
- Hosting: GitHub Pages (statico, gratuito)

---

## Licenza

Uso personale e didattico. Dati tecnici raccolti da datasheet pubblici e letteratura tecnica aperta.
