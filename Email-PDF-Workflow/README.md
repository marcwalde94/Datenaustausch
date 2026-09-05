# Email-PDF-Workflow – Nachbau-Paket

Dieses Paket beschreibt den **E-Mail-Workflow „Schulungsnachweis / One Point Lesson"** der
Handlingsfehler-Middleware so, dass eine **andere App den Look, das Layout, die Texte und die
Mechanik 1:1 nachbauen** kann – inklusive **PDF-Anhang**.

## Was ist drin?

| Datei | Inhalt |
|---|---|
| [`NACHBAU-DOKUMENTATION.md`](./NACHBAU-DOKUMENTATION.md) | **Die komplette Doku** (self-contained): Ablauf, Datenvertrag, Templates, Texte, Farben, Fonts, Versand-Technik, Outlook-Fallstricke, Checkliste. **Hier starten.** |
| [`templates/email_handlingsfehler.html`](./templates/email_handlingsfehler.html) | Die fertige HTML-Mail (Jinja2). |
| [`templates/Schulungsnachweis_Clean.html`](./templates/Schulungsnachweis_Clean.html) | Das PDF-Template (A4 quer, via Playwright → PDF). |
| [`templates/Schulungsnachweis_Large.html`](./templates/Schulungsnachweis_Large.html) | XXL-Variante (500×300mm) für Großdruck – gleiches Design. |

## Schnellstart für die neue App

1. Lies **`NACHBAU-DOKUMENTATION.md`** komplett – vor allem **Kapitel 3 (Datenvertrag)**.
2. Mappe deine eigenen Daten auf die Felder aus Kapitel 3.
3. Übernimm die beiden Templates aus `templates/` und rendere sie mit den Variablen aus Kapitel 4/5.
4. Übernimm die Texte aus Kapitel 6 wörtlich (positiver „SmartLesson"-Ton).
5. Halte die Design-Tokens (Kapitel 7) und Outlook-Regeln (Kapitel 9) ein.

## Nicht enthalten (bewusst)

- **Corporate-Fonts** (`Bree SH`, `Siemens Sans`) – lizenzpflichtig. Aus lizenzierter Quelle unter
  `templates/fonts/` ergänzen. Ohne sie greift der Arial-Fallback (Layout bleibt gleich).
- **Logo-Datei** (`siemens_logo.png`) – aus der eigenen CI beziehen.
- Interne Zugangsdaten (Graph API / SMTP).
