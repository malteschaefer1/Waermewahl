# Wärmewahl

Ein interaktives Einseiten-Dashboard, das CAPEX/OPEX, Emissionen und Förderungen einer bestehenden Ölheizung mit einer Luft-Wasser-Wärmepumpe vergleicht. **Das Projekt ist aktuell ein Work-in-Progress:** Datenmodelle, Texte und UI können sich kurzfristig ändern und werden noch validiert.

## Funktionsumfang
- editierbare Eingaben (Nutzwärmebedarf, COP, Diskontsatz, Förderpfade, Szenarien für Ölpreis, Strompreis, CO₂-Preis, Netzstromfaktor)
- deterministische Zeitreihen (Kosten, Emissionen, NPV) inklusive CSV-Export und PNG-Export der Diagramme
- Mini-Charts für CAPEX/OPEX-Aufteilung sowie tabellarische Ausgabe pro Jahr
- Dokumentation mit Modellannahmen und Quellenliste zur schnellen Nachvollziehbarkeit

## Technik-Stack
- rein statisch (`waermewahl.html`), keine Build- oder Runtime-Abhängigkeiten
- Vanilla JS für State-Handling, Chart.js 4 für Visualisierung
- CSS Grid/Flexbox + system fonts (Inter/Segoe UI) für responsive Layouts

## Nutzung lokal
1. Repository klonen oder herunterladen.
2. Datei `waermewahl.html` im Browser öffnen (Doppelklick genügt, es ist kein Server notwendig).
3. Eingaben anpassen, Ergebnisse erscheinen nach ~400 ms Debounce.

> Hinweis: Beim Arbeiten mit Browser-Storage (gespeicherte Konfiguration) empfiehlt sich ein moderner Browser; lokale Dateien sind ausreichend.

## Daten & Quellen (Auszug)
- Preis- und Szenarioannahmen: BDEW Strompreisanalyse, BMWK Monitoring, BNetzA Monitoringberichte
- Emissionsfaktoren & Klimawirkung: Umweltbundesamt, IPCC/AR6, GHG Protocol
- CO₂-Preis-Pfade: DEHSt (nEHS) sowie EU ETS2 Veröffentlichungen
- Förderlandschaft: KfW 458 / Heizungsförderung, BMWK Richtlinien
- Wärmepumpen-Performance: Fraunhofer ISE Feldtests & Projekte

Weitere Quellen sind in der App im Abschnitt „Dokumentation & Annahmen“ verlinkt.

## Roadmap / Offene Punkte
- Validierung zusätzlicher Szenarien (z. B. Gas, Mischformen)
- Bessere Vergleichbarkeit für Mehrfamilienhäuser
- i18n (derzeit nur Deutsch) und Accessibility-Feinschliff

Feedback oder Pull Requests sind willkommen – bitte im Hinterkopf behalten, dass das Modell noch iteriert wird.
