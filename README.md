Hier ist die gewünschte `README.md`-Datei für dein GitHub-Repo mit dem Titel **"Barrierefreiheit und ARIA Grundlagen"** – im stichpunktartigen Stil, ohne Demo und Fazit.

---


# Barrierefreiheit und ARIA Grundlagen

Dieses Repository enthält vier HTML-Dateien, die verschiedene Umsetzungen eines barrierefreien Kontaktformulars zeigen – von komplett unzugänglich bis vollständig semantisch mit optimalem ARIA-Einsatz.  
Ziel ist es, die Bedeutung und korrekte Anwendung von **ARIA (Accessible Rich Internet Applications)** im Web zu verstehen.

---

## 🔍 Warum Barrierefreiheit?

- Webinhalte sollen für **alle Menschen** zugänglich sein – unabhängig von Behinderung.
- **16 % der Weltbevölkerung** leben mit Einschränkungen (visuell, motorisch, auditiv, kognitiv).
- Gute Accessibility bedeutet bessere **Nutzerfreundlichkeit** für alle (z. B. klare Navigation, Tastaturbedienung).
- Gesetzlich vorgeschrieben für viele öffentliche Stellen, zunehmend relevant für Unternehmen.

---

## ✅ WCAG-Prinzipien (Web Content Accessibility Guidelines)

Barrierefreie Inhalte sollen laut WCAG folgende Prinzipien erfüllen:

- **Wahrnehmbar**: Inhalte müssen mit allen Sinnen erfassbar sein (z. B. Alt-Texte, Untertitel).
- **Bedienbar**: Alle Funktionen müssen per Tastatur steuerbar sein (z. B. Fokus-Reihenfolge).
- **Verständlich**: Inhalte und Bedienung sollen intuitiv und vorhersehbar sein.
- **Robust**: Inhalte müssen zuverlässig von Browsern und Assistive Technologies interpretierbar sein.

---

## 🧩 Was ist WAI-ARIA?

- **ARIA = Accessible Rich Internet Applications** (W3C-Standard)
- Ergänzt HTML um zusätzliche **semantische Informationen** für Screenreader & Co.
- Erforderlich v. a. bei **komplexen Widgets** (Tabs, Modals, Dropdowns), die HTML alleine nicht beschreiben kann
- ARIA wirkt **nicht sichtbar**, sondern verändert nur die Struktur im **Accessibility Tree**

### 🔄 ARIA: Kurzgeschichte & Versionen

- **ARIA 1.0** (2009): Erste Spezifikation, Fokus auf Desktop-Web
- **ARIA 1.1** (2017): Neue Rollen und bessere Unterstützung für mobile Anwendungen
- **ARIA 1.2** (2021): Ergänzungen für moderne Webtechnologien (z. B. neue Live-Regionen, `role="searchbox"`)
- **ARIA 1.3** (in Arbeit): Fokus auf Vereinfachung und Präzisierung, u. a. bessere Beziehungen zwischen Komponenten

Aktuelle Spezifikation: **ARIA 1.2** (W3C Recommendation)

---

## 🧱 ARIA-Grundbausteine

### 1. Rollen (`role`)
- Definieren, was ein Element **ist** (z. B. `button`, `navigation`, `dialog`)
- Unverzichtbar für Screenreader, wenn kein passendes HTML-Element verwendet wird

Beispiele:
```html
<div role="button" tabindex="0">Öffnen</div>
<nav role="navigation">…</nav>
````

### 2. Zustände (`aria-*`)

* Beschreiben den **aktuellen Zustand** (z. B. aufgeklappt, ausgewählt)
* Müssen dynamisch per JavaScript angepasst werden

Beispiele:

```html
<button aria-expanded="false">Menü</button>
<input aria-invalid="true">
```

### 3. Eigenschaften (`aria-*`)

* Beschreiben **zusätzliche Merkmale oder Beziehungen**
* Z. B. Beschriftung, Zugehörigkeit, Sichtbarkeit

Beispiele:

```html
<input aria-labelledby="name-label">
<input aria-describedby="error-hinweis">
<div aria-hidden="true">🎨</div>
```

---

## ⚠️ ARIA Best Practices

* **HTML First**: Immer native HTML-Elemente bevorzugen (`<button>`, `<nav>`, `<label>`)
* **No ARIA is better than bad ARIA**: Falsches ARIA schadet der Zugänglichkeit
* **Keine Redundanz**: Nicht `role="button"` auf `<button>` setzen
* **Tastaturbedienung sicherstellen**: ARIA macht keine Elemente bedienbar – das muss per JS erfolgen
* **Nur wo nötig verwenden**: ARIA ergänzt, ersetzt aber keine UX oder HTML5-Semantik
* **Testen!**: Mit Screenreadern (z. B. NVDA, VoiceOver) und Tools wie axe oder WAVE prüfen

---

## 📁 Enthaltene Dateien

| Datei                            | Beschreibung                                                    |
| -------------------------------- | --------------------------------------------------------------- |
| `01-inaccessible.html`           | Kein HTML5, kein ARIA – zeigt typische Fehler                   |
| `02-aria-no-semantics.html`     | Kein semantisches HTML, aber ARIA-Einsatz rettet Zugänglichkeit |
| `03-semantics-added-aria.html`      | HTML5 korrekt genutzt, ARIA nur wo nötig ergänzt                |
| `04-semantics-redundant-aria.html` | HTML5 korrekt, aber mit überflüssigem ARIA – Anti-Beispiel      |

---

## 📚 Weiterführende Links

* [MDN Web Docs – WAI-ARIA](https://developer.mozilla.org/de/docs/Web/Accessibility/ARIA)
* [W3C WAI-ARIA Authoring Practices](https://www.w3.org/WAI/ARIA/apg/)
* [WebAIM ARIA Introduction](https://webaim.org/techniques/aria/)
* [axe DevTools (Barrierefreiheit testen)](https://www.deque.com/axe/devtools/)

---

> **Hinweis:** Diese Dokumentation wurde mit Unterstützung einer KI (ChatGPT) erstellt und redaktionell geprüft. Alle Inhalte dürfen frei verwendet und angepasst werden.

