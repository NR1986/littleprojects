# 📘 Bedienungsanleitungen Dashboard (Offline-HTML-Viewer)

Eine moderne, vollständig offline-fähige HTML-Anwendung zur Verwaltung, Strukturierung und Anzeige von **Bedienungsanleitungen (PDFs)** – ideal für Kantinen, Werkstätten und Arbeitsplätze ohne Serverrechte oder Internetverbindung.

---

## 🌟 Features

- **100 % offline** – kein Server, keine Installation, keine externen Abhängigkeiten  
- **Moderne Dark-UI**  
- **Kategorisierung** und **intelligente Suche**  
- **Drag & Drop** zum Hinzufügen neuer PDFs  
- **Bearbeiten & Löschen** von Einträgen  
- **Import/Export** über JSON  
- **Automatisches Laden** einer *data.json* beim Start  
- **Statischer HTML-Generator** für feste, klickbare Links  
- **Saubere Trennung von Daten und Darstellung**

---

## 📁 Projektstruktur

```
kantine/
├── index.html              # Hauptanwendung
├── data.json       # Wird beim Start automatisch geladen
└── files/                  # Ordner für alle PDFs
    ├── JSKE327.pdf
    ├── JDk832.pdf
    └── ...
```

> Wichtig: Die Pfade, die in der Verwaltung eingetragen werden, **verweisen direkt auf Dateien im Ordner `files/`**.

---

## 🚀 Start & Erste Schritte

### 1. Projekt öffnen
1. Repository herunterladen oder klonen  
2. **index.html** im Browser öffnen (Chrome empfohlen)  
3. Wenn eine `data.json` vorhanden ist, wird diese  
   **automatisch geladen** und alle gespeicherten Anleitungen erscheinen sofort.

---

## 📘 Nutzung: Anleitungen anzeigen

Im Tab **„📘 Anleitungen“** findest du:

- eine **Suchleiste**
- **Kategorien-Chips**
- eine **übersichtliche Kartenansicht**
- blaue **„Öffnen“-Buttons** für jede PDF

Die PDFs öffnen sich in einem **neuen Tab**.

---

## ⚙️ Verwaltung

Der Verwaltungsbereich erlaubt:

### 🔹 Anleitungen hinzufügen
- PDFs in das Feld **„PDFs hierher ziehen“** ziehen  
- oder auf die Fläche klicken & mehrere auswählen

Neue Einträge werden automatisch erzeugt.

### 🔹 Einträge bearbeiten

Pro Anleitung kannst du einstellen:

| Feld | Bedeutung |
|------|-----------|
| **Titel** | Der angezeigte Name in der Übersicht |
| **Pfad** | Relativer Speicherort, z. B. `files/Jura.pdf` |
| **Kategorie** | Themenbereich (mit Autovervollständigung) |

### 🔹 Einträge löschen
Einfach **„Löschen“** drücken.

---

## 📤 Export / 📥 Import

### Exportieren
Speichert alle Einträge als **data.json**

### Importieren
Beliebige zuvor exportierte Datei auswählen →  
Alle Einträge werden sofort übernommen.

---

## 🛠 Automatisches Laden der `data.json`

Wenn kein localStorage vorhanden ist:

- lädt die App automatisch `data.json`
- übernimmt **Titel**, **Pfade**, **Kategorien**

Ideal für Terminals oder PC-Arbeitsplätze.

---

## 🧱 Statisches HTML erzeugen

Für komplett fertige Systeme:

1. Verwaltung öffnen  
2. Nach unten scrollen  
3. **„HTML-Code erzeugen“** klicken  
4. Code kopieren → in eine Datei `index_static.html` speichern  

Diese Version enthält **nur noch die Links**, ohne Verwaltungsoberfläche.

---

## 🔐 Datenschutz & Sicherheit

- Keine Serververbindungen  
- PDFs werden nur referenziert, nicht verändert  
- JSON-Dateien bleiben lokal  
- Daten werden niemals ins Internet übertragen  

---

## 🔧 Technische Details

| Komponente | Details |
|-----------|---------|
| Sprache | HTML, CSS, JavaScript (Vanilla) |
| Speicherung | localStorage + JSON |
| PDF-Verweise | relative Pfade (`files/...`) |
| Browser | Chrome/Edge empfohlen |
| Frameworks | keine |

---

## ❓ FAQ

**PDF öffnet nicht?**  
→ Pfad prüfen: `files/...`

**Keine Anleitungen sichtbar?**  
→ `data.json` fehlt oder ist leer

**Kann ich das Projekt auf mehrere PCs kopieren?**  
→ Ja. Einfach den gesamten Ordner kopieren.

---

## ✨ Autor & Version

**Nino Rossi**  
Stand: November 2025  
Version: 1.5  
