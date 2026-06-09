# Een Tweede Thuis — Design System & Style Guide

> Stijlgids voor de website, afgeleid van het logo. Plak dit in Claude Design als basisbriefing.

---

## 1. Merkpersoonlijkheid

| Eigenschap | Uitleg |
|---|---|
| **Warm** | Het logo straalt geborgenheid uit: een huis, een zon, mensen die elkaar vasthouden. |
| **Verbindend** | Drie figuren (oranje, groen, blauw) houden elkaar vast — diversiteit en samenkomst. |
| **Optimistisch** | Felle, levendige kleuren en een stralende zon. Geen somberheid. |
| **Toegankelijk** | Ronde vormen, handgeschreven titel, niets klinisch of afstandelijk. |
| **Veilig & stabiel** | "Thuis" in rustige teal verankert het geheel. |

**Kernbelofte:** een plek waar je je welkom, gezien en geborgen voelt — een tweede thuis.

---

## 2. Kleurenpalet

Afgeleid uit het logo. Oranje is primair (huis, warmte, energie), teal is secundair (vertrouwen, rust, "thuis").

### Primair

| Kleur | Hex | Gebruik |
|---|---|---|
| 🟧 Huisoranje | `#F4791F` | Primaire knoppen, accenten, koppen, logohuiskleur |
| 🟥 Dakrood | `#E63B2E` | Hover-staten, nadruk, call-to-action verlopen |
| 🟦 Thuis-teal | `#15807C` | Secundaire knoppen, links, "Thuis"-toon, footers |

### Accenten

| Kleur | Hex | Gebruik |
|---|---|---|
| 🟨 Zonnegeel | `#FDB827` | Highlights, badges, iconen, warme accenten |
| 🟩 Grasgroen | `#5BAA36` | Succes-meldingen, natuur/groei, illustraties |
| 🟦 Hemelblauw | `#2B8CCC` | Info-meldingen, secundaire iconen, vogel/lucht |
| 🟦 Diepblauw | `#1B6FB3` | Tekstlinks op lichte vlakken, donkere blauwe figuur |

### Neutralen

| Kleur | Hex | Gebruik |
|---|---|---|
| Warmwit | `#FFFBF6` | Paginabodem (warmer dan puur wit) |
| Zachtcrème | `#FFF3E6` | Sectie-achtergronden, cards |
| Lichtgrijs | `#EDE7E0` | Randen, scheidingslijnen |
| Antraciet | `#2E2A26` | Bodytekst (warme zwart, geen koud zwart) |
| Middengrijs | `#6E665E` | Secundaire tekst, bijschriften |

### Verlopen

```
--gradient-warm:   linear-gradient(135deg, #FDB827 0%, #F4791F 55%, #E63B2E 100%);  /* zon → dak */
--gradient-thuis:  linear-gradient(135deg, #2B8CCC 0%, #15807C 100%);               /* lucht → thuis */
```

### CSS-variabelen (kopieer-klaar)

```css
:root {
  /* Primair */
  --color-primary:        #F4791F;
  --color-primary-dark:   #E63B2E;
  --color-secondary:      #15807C;

  /* Accenten */
  --color-sun:    #FDB827;
  --color-grass:  #5BAA36;
  --color-sky:    #2B8CCC;
  --color-deep:   #1B6FB3;

  /* Neutralen */
  --color-bg:           #FFFBF6;
  --color-surface:      #FFF3E6;
  --color-border:       #EDE7E0;
  --color-text:         #2E2A26;
  --color-text-muted:   #6E665E;

  /* Status */
  --color-success: #5BAA36;
  --color-info:    #2B8CCC;
  --color-warning: #FDB827;
  --color-danger:  #E63B2E;

  /* Verlopen */
  --gradient-warm:  linear-gradient(135deg, #FDB827 0%, #F4791F 55%, #E63B2E 100%);
  --gradient-thuis: linear-gradient(135deg, #2B8CCC 0%, #15807C 100%);
}
```

---

## 3. Typografie

Het logo combineert een **handgeschreven script** ("Een Tweede / Thuis") met warmte. Vertaal dat naar het web met een levendige titelfont en een vriendelijke, ronde leesfont.

| Rol | Font | Alternatief | Toelichting |
|---|---|---|---|
| **Display / logo-titel** | `Pacifico` of `Caveat` | `Comfortaa` | Alleen voor grote titels of het woordmerk, spaarzaam gebruiken |
| **Koppen (H1–H3)** | `Poppins` (600/700) | `Nunito` | Rond, vriendelijk, modern |
| **Bodytekst** | `Nunito` (400/600) | `Open Sans` | Zacht, goed leesbaar, warm |

```css
:root {
  --font-display: 'Pacifico', cursive;
  --font-heading: 'Poppins', sans-serif;
  --font-body:    'Nunito', sans-serif;
}
```

### Schaal (type scale)

| Element | Grootte | Gewicht | Regelafstand |
|---|---|---|---|
| H1 | 2.75rem (44px) | 700 | 1.15 |
| H2 | 2rem (32px) | 700 | 1.2 |
| H3 | 1.5rem (24px) | 600 | 1.3 |
| Body | 1.0625rem (17px) | 400 | 1.65 |
| Klein / bijschrift | 0.875rem (14px) | 400 | 1.5 |

> **Tip:** zet titels in `--color-primary` of `--color-secondary`, nooit beide door elkaar in één blok. Body altijd in `--color-text`.

---

## 4. Vorm & ruimte

Het logo is volledig rond en organisch. Vermijd scherpe hoeken.

```css
:root {
  --radius-sm:  10px;
  --radius-md:  18px;
  --radius-lg:  28px;
  --radius-pill: 999px;

  --shadow-soft: 0 6px 20px rgba(46, 42, 38, 0.08);
  --shadow-lift: 0 12px 32px rgba(244, 121, 31, 0.18);

  --space-xs: 8px;
  --space-sm: 16px;
  --space-md: 24px;
  --space-lg: 48px;
  --space-xl: 80px;
}
```

- **Hoeken:** alles afgerond (cards `--radius-lg`, knoppen `--radius-pill`).
- **Schaduwen:** zacht en warm, nooit hard zwart.
- **Witruimte:** royaal — geeft rust, past bij "geborgenheid".

---

## 5. Componenten

### Knoppen

```css
/* Primair — call to action */
.btn-primary {
  background: var(--gradient-warm);
  color: #fff;
  border-radius: var(--radius-pill);
  padding: 14px 28px;
  font-family: var(--font-heading);
  font-weight: 600;
  box-shadow: var(--shadow-lift);
  border: none;
}
.btn-primary:hover { filter: brightness(0.95); transform: translateY(-1px); }

/* Secundair — rustig */
.btn-secondary {
  background: var(--color-secondary);
  color: #fff;
  border-radius: var(--radius-pill);
  padding: 14px 28px;
}

/* Tertiair — outline */
.btn-outline {
  background: transparent;
  color: var(--color-primary);
  border: 2px solid var(--color-primary);
  border-radius: var(--radius-pill);
  padding: 12px 26px;
}
```

### Cards

```css
.card {
  background: #fff;
  border-radius: var(--radius-lg);
  padding: var(--space-md);
  box-shadow: var(--shadow-soft);
  border: 1px solid var(--color-border);
}
.card-accent { border-top: 5px solid var(--color-sun); }
```

### Secties

- **Hero:** warmwitte of crème achtergrond, grote vriendelijke titel, één primaire knop. Eventueel een zachte golfvorm onderaan (verwijst naar het gras/heuvel in het logo).
- **Afwisseling:** wissel `--color-bg` en `--color-surface` per sectie voor ritme.
- **Footer:** in `--color-secondary` (teal) met witte tekst — verankert de pagina zoals "Thuis" het logo verankert.

### Golf-/heuvelvorm (signatuurelement)

Het logo heeft een groene heuvel onderaan. Gebruik een zachte SVG-golf als sectiescheiding:

```html
<svg viewBox="0 0 1440 80" preserveAspectRatio="none" style="display:block;width:100%;height:60px">
  <path d="M0,40 C360,90 1080,-10 1440,40 L1440,80 L0,80 Z" fill="#5BAA36"/>
</svg>
```

---

## 6. Iconografie & beeldtaal

- **Iconen:** ronde, gevulde of dik-lijnige iconen (bijv. Phosphor "fill", Lucide met dikke stroke). Geen dunne, scherpe lijniconen.
- **Illustratiestijl:** vlakke, kleurrijke illustraties met verlopen — in lijn met het logo. Mensen, huizen, natuur, handen.
- **Foto's:** warm, natuurlijk licht, echte mensen, geen zakelijke stockfoto's. Lichte warme kleurcorrectie.
- **Kernmotieven uit het logo:** huis 🏠, zon ☀️, handen/verbinding 🤝, groen/natuur 🌿, vogel 🕊️ (vrijheid).

---

## 7. Tone of voice

| Wel | Niet |
|---|---|
| Warm, persoonlijk, "jij/je" | Afstandelijk, "men/u" overal |
| Concreet en geruststellend | Vaag of ambtelijk |
| Uitnodigend ("Welkom thuis") | Eisend of klinisch |
| Korte, heldere zinnen | Jargon en lange volzinnen |

Voorbeeld microcopy: *"Welkom. Hier hoor je erbij."* · *"Kom langs en voel je thuis."* · *"Samen sterker."*

---

## 8. Do's & don'ts

✅ **Do**
- Oranje als hoofdaccent, teal als rustpunt.
- Royale witruimte en afgeronde vormen.
- Warme neutralen (`#FFFBF6`) i.p.v. koud wit.
- Eén display-/scriptfont, spaarzaam ingezet.

❌ **Don't**
- Alle vijf kleuren tegelijk in één blok (wordt rommelig).
- Scherpe hoeken of harde zwarte schaduwen.
- Koud blauwgrijs als achtergrond.
- Script-font voor bodytekst (onleesbaar).

---

## 9. Snelle briefing voor Claude Design (kopieer-klaar)

> Bouw een warme, gemeenschapsgerichte website voor "Een Tweede Thuis". Primaire kleur warm oranje `#F4791F` met verloop naar rood `#E63B2E`; secundaire kleur teal `#15807C`; accenten zonnegeel `#FDB827`, grasgroen `#5BAA36`, hemelblauw `#2B8CCC`. Achtergrond warmwit `#FFFBF6`, tekst antraciet `#2E2A26`. Koppen in Poppins, body in Nunito, optioneel Pacifico voor het woordmerk. Alles afgerond (pill-knoppen, cards met 28px radius), zachte warme schaduwen, royale witruimte. Footer in teal. Gebruik zachte golfvormen als sectiescheiding (verwijzend naar de groene heuvel in het logo). Toon: warm, uitnodigend, geruststellend.
