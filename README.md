# Tauch mit mir ab — Website

Static website built with [Jekyll](https://jekyllrb.com/) and the Minima theme.

---

## Inhalte bearbeiten

Alle Seiteninhalte befinden sich in Markdown-Dateien (`.md`) im Hauptverzeichnis. Diese können direkt auf GitHub im Browser bearbeitet werden — kein lokales Setup nötig.

| Datei | Inhalt |
|---|---|
| `index.md` | Startseite |
| `faq.md` | FAQ |
| `anreise.md` | Anreise, Karte, Shuttle |

### Markdown-Grundlagen

```
## Überschrift

Normaler Text einfach hinschreiben.

**fett**, *kursiv*

[Linktext](https://example.com)

- Listenpunkt 1
- Listenpunkt 2
```

Zeilenumbruch ohne neuen Absatz: zwei Leerzeichen am Zeilenende.

### Navigationsreihenfolge ändern

In `_config.yml` unter `header_pages` die Reihenfolge der Dateien anpassen.

### Neue Seite hinzufügen

1. Neue Datei `seitenname.md` erstellen mit folgendem Kopf:
   ```
   ---
   layout: page
   title: Seitentitel
   permalink: /seitenname/
   ---
   ```
2. Dateiname in `_config.yml` unter `header_pages` eintragen.

---

## Lokal vorschauen (optional)

Voraussetzung: Ruby und Bundler installiert.

```bash
bundle install
bundle exec jekyll serve
```

Dann im Browser: `http://localhost:4000`

---

## Deployment

Die Website wird auf **GitHub Pages** gehostet. Nach jedem Push auf den `main`-Branch wird die Seite automatisch aktualisiert — kein manueller Schritt nötig.

Setup (einmalig): Repository-Einstellungen → Pages → Source: **Deploy from branch** → Branch: `main` / `/ (root)`.
