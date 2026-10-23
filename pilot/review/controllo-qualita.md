# Controllo di qualità — Pilota V1
**Data:** 23/10/2026  
**Rama:** pilot/creative-activities-v1  
**Verificato da:** Claude Code (verifica digitale — non testato su stampante fisica)

---

## 1. Archivi modificati

| Archivo | Operazione | Note |
|---------|-----------|------|
| `pilot/fichas/ficha-01-il-mio-mondo-di-colori.html` | Aggiornato | Sostituita immagine Lupino da base64 (~142 KB) a `../img/char-lupino.png`. Riduzione da 153 KB a 11 KB. Nessuna modifica visiva. |
| `pilot/fichas/ficha-02-la-mia-casa-speciale.html` | Creato (nuovo) | Sostituisce `ficha-02-da-una-macchia-a-una-storia.html`, che rimane come backup. |
| `pilot/fichas/ficha-03-un-animale-fantastico.html` | Creato (nuovo) | Sostituisce `ficha-03-la-casa-delle-forme.html`, che rimane come backup. |
| `pilot/review/ficha-01.png` | Generato | Render PNG finale. |
| `pilot/review/ficha-02.png` | Generato | Render PNG finale. |
| `pilot/review/ficha-03.png` | Generato | Render PNG finale. |
| `pilot/review/pilota-v1.pdf` | Generato | PDF a 3 pagine, una per attività. |

**Archivi precedenti conservati (non cancellati):**
- `pilot/fichas/ficha-01-v1-backup.html` — backup v1 originale
- `pilot/fichas/ficha-02-da-una-macchia-a-una-storia.html` — backup ficha-02 precedente
- `pilot/fichas/ficha-03-la-casa-delle-forme.html` — backup ficha-03 precedente

---

## 2. Risorse grafiche

### Utilizzate (PNG originali — `pilot/img/`)
| File | Dimensioni | Usato in |
|------|-----------|---------|
| `char-lupino.png` | 1254 × 1254 px, RGB | ficha-01 (immagine accompagnatrice) |
| `char-nubola.png` | 1254 × 1254 px, RGB | ficha-02 (header + SVG inline nel canvas) |
| `char-cubetto.png` | 1254 × 1254 px, RGB | ficha-03 (header + SVG inline nel canvas) |

Nota: nei canvas delle fichas 02 e 03 il personaggio appare sia come `<img>` nel header (PNG) sia come SVG inline piccolo nell'angolo del canvas (ridisegno fedele inline per il fumetto). Le PNG originali NON sono state rigenerate né ridisegnate — il personaggio principale è sempre la PNG.

### Risorse mancanti
- Nessuna risorsa mancante per la produzione del pilota.
- I PDF dei prodotti reali (E1, E2, E3, B1, B2, B3) non esistono ancora — fuori scope del pilota.

---

## 3. Dimensioni e formato

| Elemento | Specifica | Risultato |
|---------|-----------|---------|
| Formato pagina | A4 (210 × 297 mm) | ✅ Conforme — `width:210mm`, `@page{size:A4}` |
| PDF | 3 pagine, una per attività | ✅ — 7,9 MB |
| PNG render | ~1240 × 1754 px @ 1,5× | ✅ — ficha-01: 223 KB, ficha-02: 186 KB, ficha-03: 193 KB |
| Stampa colore | `print-color-adjust:exact` dichiarato | ✅ in tutte e tre le fichas |
| Stampa B&N | Contorni scuri (#3D2B1A), zone aperte | ✅ leggibile in B&N — le zone da colorare restano vuote e leggibili |

---

## 4. Margini e leggibilità

### Verificato digitalmente:

**Ficha-01 — Il mio mondo di colori:**
- ✅ Margini sicuri — nessun elemento tagliato ai bordi.
- ✅ Consigna leggibile (13 pt bold sopra il canvas).
- ✅ Varianti per età (3/4/5 anni) leggibili.
- ✅ Lupino PNG visibile nell'angolo in basso a sinistra.
- ⚠️ Il fumetto di Lupino ("Colora!") è parzialmente visibile — il testo appare abbreviato nel render del canvas. Non causa confusione ma è un dettaglio da valutare.

**Ficha-02 — La mia casa speciale:**
- ✅ Margini sicuri — nessun elemento tagliato.
- ✅ Casa con tetto organico, camino, due finestre con croce, porta tratteggiata.
- ✅ Alberi con chiome arrotondate a "nuvola" (corretti dopo prima revisione: le versioni iniziali avevano rami incrociati visivamente simili a X).
- ✅ Recinzione, sentiero, zone "Aggiungi i fiori!" con bordo tratteggiato.
- ✅ Nubola con fumetto "La tua!" nell'angolo del giardino.
- ✅ Zona cielo superiore (≈40% del canvas) lasciata intenzionalmente bianca per disegno libero.
- ⚠️ La zona cielo bianca nella metà superiore del canvas potrebbe sembrare "vuota" prima di capire che è spazio per disegnare — valutare se aggiungere un prompt leggero ("Disegna il cielo!") in una versione successiva.

**Ficha-03 — Un animale fantastico:**
- ✅ Testa dell'animale (occhi, naso, bocca, baffi, orecchie) chiaramente disegnata come punto di partenza.
- ✅ Badge "La testa è pronta! ✓" visibile.
- ✅ Zone tratteggiate per corpo, zampe, coda, ali/pinne — leggibili e separate.
- ✅ Cerchi colori ("Di che colore è?") e linea nome a sinistra.
- ✅ Cubetto con fumetto "Fantastico!".
- ✅ Zona "Dove vive?" aggiunta nel terzo superiore del canvas con bordo tratteggiato e testo guida.
- ⚠️ **Problema noto:** la zona "Dove vive?" (rettangolo tratteggiato) si sovrappone leggermente al bordo superiore della testa dell'animale. Visivamente leggibile ma potrebbe creare confusione su dove finisce la zona ambiente e dove inizia la testa. Da valutare: abbassare la testa di ~50px o ridurre l'altezza della zona "Dove vive?".
- ⚠️ Attività diversa dalle fichas 01 e 02 ✅ — ma la distinzione tra "zona dove vive" e "zona corpo" richiede la mediazione dell'adulto per i bambini di 3 anni.

---

## 5. Problemi rilevati e correzioni applicate

| Problema | Gravità | Stato |
|---------|---------|-------|
| Ficha-01: Lupino embedato come base64 (153 KB, difficile da aggiornare) | Tecnico | ✅ Corretto — ora usa `../img/char-lupino.png` |
| Ficha-02 (prima versione): alberi con rami che attraversavano la chioma (effetto X) | Visivo | ✅ Corretto — chiome bubbly organiche senza rami interni |
| Ficha-03: zona superiore del canvas non aveva invito esplicito | UX | ✅ Corretto — aggiunta zona "Dove vive?" tratteggiata |
| Ficha-03: zona "Dove vive?" si sovrappone leggermente alla testa | Visivo lieve | ⚠️ Documentato — richiede valutazione umana |

---

## 6. Coerenza visiva tra le fichas

| Elemento | F-01 | F-02 | F-03 |
|---------|------|------|------|
| Font: Bricolage Grotesque + DM Sans | ✅ | ✅ | ✅ |
| Header dark (#173D35) con titolo bianco | ⚠️ Diverso* | ✅ | ✅ |
| Fondo pagina: crema (#F8F1E4) | ❌ Bianco** | ✅ | ✅ |
| Personaggio in header (PNG) | ✅ img | ✅ img | ✅ img |
| Canvas bianco con bordo scuro | ✅ | ✅ | ✅ |
| Consigna con bordo colorato sotto il canvas | ❌ Sopra*** | ✅ | ✅ |
| Varianti 3/4/5 anni (barra scura) | ✅ | ✅ | ✅ |
| Footer con nome prodotto e numerazione | ✅ | ✅ | ✅ |
| Colore accent per varianti | Arancione | Blu | Viola |

*\* Ficha-01 usa il design del header precedente (flat, senza box arrotondato). È il risultato della revisione v3 già approvata in sessione precedente — non modificata senza autorizzazione.  
** Ficha-01 ha fondo pagina bianco invece di crema — è il design originale v3.  
*** Ficha-01 ha la consigna sopra il canvas invece che sotto — è il design originale v3.

**Decisione raccomandata:** uniformare il design di ficha-01 a quello delle fichas 02/03 (header verde, fondo crema, consigna sotto) OPPURE tenere intenzionalmente lo stile diverso come "variante più semplice" per bambini più piccoli. Questa decisione spetta alla responsabile del prodotto.

---

## 7. Test di stampa

**Non testato su stampante fisica.** Verifica digitale effettuata tramite:
- Render PNG a 1240×1754 px (equivalente ~150 dpi su A4)
- Export PDF via Playwright/Chromium con `@page{size:A4}` e `print-background:true`

Elementi da verificare nella prima stampa reale:
- Spessore contorni (2.5–3 px in SVG) — potrebbe variare leggermente con diversi driver di stampa
- Colori piatti (#173D35, #F8F1E4) — devono rimanere leggibili a colori
- In B&N: le zone tratteggiate (porta, fiori, corpo animale) restano visibili

---

## 8. Aspetti che richiedono approvazione umana

1. **Design di ficha-01**: mantenere il layout v3 (diverso da 02/03) o uniformare?
2. **Zona "Dove vive?" in ficha-03**: accettare la leggera sovrapposizione con la testa, o riposizionare?
3. **Zona cielo di ficha-02**: aggiungere un prompt ("Disegna il cielo!") o lasciare libero?
4. **Personaggi inline nei canvas**: le versioni SVG piccole di Nubola e Cubetto nel canvas sono fedeli ma non identiche alle PNG — confermare se sono accettabili o se si preferisce usare le PNG originali anche lì (richiederebbe absolute positioning).
5. **Testimonianze per Lupino**: il fumetto di Lupino è visibile ma piccolo in ficha-01 — valutare se ingrandire.

---

*Produzione pronta per revisione umana. Nessuna delle 27 fichas restanti è stata creata.*  
*Approvazione finale spetta alla responsabile del prodotto.*
