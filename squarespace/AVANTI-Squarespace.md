# AVANTI – Squarespace-Paket

Zum Einfügen in `avantiservices.squarespace.com`. Reihenfolge: 1. CSS, 2. Seiten anlegen, 3. Texte, 4. Formular.

Ausgangspunkt war die App (`index.html`): Schwarz `#080808`, Gold `#c9a45b`, Weiß `#f5f5f2`, Slogan **EINFACH. WEITER.**

---

## 1. Design → Eigenes CSS

Squarespace: **Website → Design → Eigenes CSS** (Custom CSS). Alles einfügen.

```css
/* AVANTI – Dark & Gold */
:root {
  --av-black: #080808;
  --av-card: #151515;
  --av-white: #f5f5f2;
  --av-gray: #999995;
  --av-gold: #c9a45b;
  --av-line: rgba(255,255,255,.09);
}

body, .page-section, .sqs-block-html, #siteWrapper {
  background: var(--av-black) !important;
  color: var(--av-white) !important;
  font-family: -apple-system, BlinkMacSystemFont, "SF Pro Display", "Helvetica Neue", Arial, sans-serif;
}

h1, h2, h3, h4 { color: var(--av-white) !important; letter-spacing: .02em; }
h1 { font-weight: 800; letter-spacing: .12em; }
p, li { color: var(--av-gray) !important; line-height: 1.7; }
a { color: var(--av-gold); }

/* Buttons */
.sqs-block-button-element,
.sqs-button-element--primary {
  background: var(--av-white) !important;
  color: #080808 !important;
  border: none !important;
  border-radius: 15px !important;
  font-weight: 700;
  padding: 17px 34px;
}
.sqs-button-element--secondary {
  background: transparent !important;
  color: var(--av-gold) !important;
  border: 1px solid var(--av-gold) !important;
  border-radius: 15px !important;
}

/* Formular */
.form-wrapper input, .form-wrapper textarea, .form-wrapper select {
  background: var(--av-card) !important;
  border: 1px solid var(--av-line) !important;
  border-radius: 15px !important;
  color: var(--av-white) !important;
  padding: 16px;
}
.form-wrapper input:focus, .form-wrapper textarea:focus {
  border-color: rgba(201,164,91,.65) !important;
}

/* Karten (Leistungen / Partner) */
.av-card {
  background: var(--av-card);
  border: 1px solid var(--av-line);
  border-radius: 20px;
  padding: 24px;
}
.av-card h3 { margin-bottom: 8px; }
.av-gold { color: var(--av-gold) !important; }
```

---

## 2. Seitenstruktur (Pages → Hauptnavigation)

| Reihenfolge | Seite | URL |
|---|---|---|
| 1 | Start | `/` |
| 2 | Leistungen | `/leistungen` |
| 3 | Partner | `/partner` |
| 4 | Anfrage | `/anfrage` |
| 5 | Kontakt | `/kontakt` |
| Fußzeile | Impressum, Datenschutz | `/impressum`, `/datenschutz` |

Impressum und Datenschutz sind in Deutschland Pflicht. Die Angaben dafür musst du liefern.

---

## 3. Texte

### Start

**Überschrift (H1):** AVANTI

**Unterzeile:** EINFACH. WEITER.

**Intro:**
Du hast ein Anliegen, wir kümmern uns darum. AVANTI verbindet dich mit geprüften Partnern aus Solingen und Umgebung – von Handwerk über Versicherungen bis zu Events. Eine Anfrage, ein Ansprechpartner.

**Button:** Anfrage stellen → `/anfrage`
**Zweiter Button:** Partner entdecken → `/partner`

**Abschnitt „So funktioniert's"** (3 Spalten):
1. **Anfrage senden** – Sag uns kurz, worum es geht und wo.
2. **Wir kümmern uns** – AVANTI findet den passenden Partner und koordiniert alles.
3. **Du kommst weiter** – Du bekommst Rückmeldung, Angebot und Umsetzung aus einer Hand.

### Leistungen

**H1:** Was AVANTI für dich übernimmt

Vier Karten:
- **Handwerk & Technik** – Zum Beispiel Elektriker: Installation und Prüfung von Elektroanlagen.
- **Versorgungskonzepte** – Laufende Versorgung für Unternehmen, sauber geplant.
- **Veranstaltungen** – Planung und Organisation, inklusive Partnern für Catering und Location.
- **Versicherungen, Immobilien & Kredite** – Beratung über erfahrene Partner.

**Button:** Jetzt anfragen → `/anfrage`

### Partner

**H1:** Unsere Partner

- **Salvatore Abbate** – Versicherungen · Immobilien · Kredite
- **Tony Pisano** – Mobiler Pizzabäcker · Catering
- **Hofgarten Solingen** – Shopping · Freizeit · Events

**Abschluss:** Du möchtest AVANTI Partner werden? Schreib uns über die Kontaktseite.

### Anfrage

**H1:** Neue AVANTI Anfrage

**Intro:** Erzähl uns kurz, worum es geht. Wir melden uns schnellstmöglich.

Formular: siehe Abschnitt 4.

### Kontakt

**H1:** Kontakt

**Text:** Fragen, Ideen oder Partnerschaft? Wir freuen uns auf deine Nachricht.

*(E-Mail, Telefon und Adresse trägst du ein. Die App-Daten enthalten keine.)*

---

## 4. Anfrage-Formular (Formularblock)

Auf der Seite `/anfrage`: **Block hinzufügen → Formular**. Felder:

| Feld | Typ | Pflicht |
|---|---|---|
| Name | Name | ja |
| E-Mail | E-Mail | ja |
| Telefon | Telefon | nein |
| Worum geht es? | Einzeiliger Text | ja |
| Ort | Einzeiliger Text | ja |
| Kategorie | Dropdown: Handwerk & Technik, Versorgung, Veranstaltung, Versicherung/Immobilien/Kredit, Sonstiges | ja |
| Beschreibung | Mehrzeiliger Text | nein |
| Datenschutz | Kontrollkästchen „Ich stimme der Datenschutzerklärung zu" | ja |

Speicherort: **Speicher → E-Mail** an deine Adresse. Absende-Button: „Anfrage senden". Bestätigungstext: „Danke! Wir kümmern uns darum und melden uns."

---

## 5. Noch offen (braucht dich)

- Impressum und Datenschutz (rechtliche Angaben)
- Kontaktdaten
- Logo (Wortmarke „AVANTI" in Weiß, Sperrung ca. 7 px)
- Fotos der Partner, falls gewünscht
- Domain-Verbindung, falls noch nicht erfolgt
