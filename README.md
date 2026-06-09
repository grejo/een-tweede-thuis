# Een Tweede Thuis

Website voor **Een Tweede Thuis** — een warme, laagdrempelige plek in Genk waar
niet-begeleide minderjarige vluchtelingen tussen 12 en 23 jaar terechtkunnen voor
ontspanning, ontmoeting, begeleiding en ondersteuning.

> „Thuis is niet altijd een plek, soms is het een gevoel — en dat gevoel willen wij meegeven.”

## Over deze site

Een statische website (HTML + CSS + een beetje JavaScript), opgebouwd in de huisstijl
uit de styleguide: warm oranje, thuis-teal, afgeronde vormen, vriendelijke typografie
(Pacifico / Poppins / Nunito) en zachte golfvormen als sectiescheiding.

### Secties
- **Hero** met kernbelofte
- **Missie & Visie**
- **Het team** — de vijf organisatoren met foto
- **Plattegrond** en **locatiekaart** (klikbaar → full-screen lightbox)
- **Bezoek ons** met adres, openingsuren en contact

## Lokaal bekijken

Geen build-stap nodig. Start een eenvoudige webserver in de projectmap:

```bash
python3 -m http.server 8123
```

Open daarna [http://localhost:8123/](http://localhost:8123/).

## Deployen naar Netlify

De `netlify.toml` is al ingesteld (`publish = "."`). Twee opties:

1. **Drag & drop** — sleep de projectmap naar [app.netlify.com/drop](https://app.netlify.com/drop).
2. **Git** — koppel deze repository aan Netlify; geen build command nodig.

## Structuur

```
.
├── index.html
├── netlify.toml
├── assets/
│   ├── css/style.css
│   └── images/          # logo, teamfoto's, plattegrond, kaart
└── een-tweede-thuis-styleguide.md
```
