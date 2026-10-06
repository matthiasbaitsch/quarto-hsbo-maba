# quarto-hsbo-maba

Quarto-Extension mit dem gemeinsamen Aussehen meiner Lehrveranstaltungen an der Hochschule Bochum
(Folien und HTML-Seiten).

## Formate

| Format | Basis | Inhalt |
|---|---|---|
| `hsbo-maba-revealjs` | revealjs | Folien-Stil, Titelfolie mit Logo, gemeinsame Optionen |
| `hsbo-maba-html` | html | Stil für HTML-Seiten (Aufgaben) |

## Einbinden

```bash
quarto add matthiasbaitsch/quarto-hsbo-maba
```

Danach in `_quarto.yml` oder im Dokument:

```yaml
format:
  hsbo-maba-revealjs: default
  hsbo-maba-html: default
```

Lokale Optionen in `_quarto.yml` überschreiben die der Extension. Den Ordner `_extensions/` im Projekt
einchecken.

## Aktualisieren

```bash
quarto update matthiasbaitsch/quarto-hsbo-maba
```

## Testen

`template.qmd` (Folien) und `template-html.qmd` (HTML) enthalten die Elemente, die das Stylesheet
besonders behandelt.

```bash
quarto render template.qmd
quarto render template-html.qmd
```

## Bekannte Meldungen

- `Cannot read properties of undefined (reading 'Config')` in der Browser-Konsole und beim PDF-Export
  mit Decktape: Das Reveal-Mathe-Plugin ruft nach dem Laden `MathJax.Hub.Config` (MathJax-2-API) auf,
  MathJax 4 kennt das nicht. Harmlos, die Formeln setzt MathJax 4 trotzdem.
