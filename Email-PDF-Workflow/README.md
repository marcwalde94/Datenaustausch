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
| [`assets/siemens_logo_email.png`](./assets/siemens_logo_email.png) | Siemens-Healthineers-Logo für die **E-Mail** (Header, via CID). |
| [`assets/siemens_logo_pdf.png`](./assets/siemens_logo_pdf.png) | Siemens-Healthineers-Logo für das **PDF** (Header, via Base64). |

## Schnellstart für die neue App

1. Lies **`NACHBAU-DOKUMENTATION.md`** komplett – vor allem **Kapitel 3 (Datenvertrag)**.
2. Mappe deine eigenen Daten auf die Felder aus Kapitel 3.
3. Übernimm die beiden Templates aus `templates/` und rendere sie mit den Variablen aus Kapitel 4/5.
4. Übernimm die Texte aus Kapitel 6 wörtlich (positiver „SmartLesson"-Ton).
5. Halte die Design-Tokens (Kapitel 7) und Outlook-Regeln (Kapitel 9) ein.

## Enthaltene Assets

- **Siemens-Healthineers-Logo** liegt in [`assets/`](./assets) – in zwei Varianten:
  `siemens_logo_email.png` (E-Mail, via CID) und `siemens_logo_pdf.png` (PDF, via Base64).
  Beide sind dieselbe Bildmarke in unterschiedlicher Auflösung/Zuschnitt.

## Nicht enthalten (bewusst)

- **Corporate-Fonts** (`Bree SH`, `Siemens Sans`) – lizenzpflichtig. Aus lizenzierter Quelle unter
  `templates/fonts/` ergänzen. Ohne sie greift der Arial-Fallback (Layout bleibt gleich).
- Interne Zugangsdaten (Graph API / SMTP).
