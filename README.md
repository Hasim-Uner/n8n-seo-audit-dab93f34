# Automated SEO & Conversion Audit

Öffentlicher, bereinigter Workflow-Export eines automatisierten Website-Audits. Das System kombiniert technische Performance-Daten mit einer strukturierten Content- und Conversion-Analyse und erzeugt daraus einen PDF-Report.

## Was der Workflow macht

1. URL über einen Webhook entgegennehmen
2. Website-Inhalt abrufen
3. Google PageSpeed Insights für Mobile auswerten
4. Lighthouse-Daten auf relevante Kennzahlen und Probleme reduzieren
5. Technische Ergebnisse durch einen Analyse-Agenten aufbereiten
6. Website-Texte auf Klarheit und Conversion-Leaks untersuchen
7. Handlungsempfehlungen in einen Report überführen
8. HTML in PDF konvertieren und versenden

## Architektur

```text
Webhook
  ↓
Website-Fetch
  ↓
PageSpeed Insights
  ↓
Datenfilter
  ↓
Tech-Analyse
  ↓
Content-/Conversion-Analyse
  ↓
Strategie-Aufbereitung
  ↓
HTML-Report
  ↓
PDF
  ↓
E-Mail
```

## Schwerpunkte

- technische SEO- und Performance-Diagnostik
- Core-Web-Vitals-nahe Kennzahlen wie LCP und CLS
- priorisierte technische Probleme
- Positionierungs- und Verständlichkeitsanalyse
- Conversion-Leaks und CTA-Optimierung
- automatisierte Report-Erstellung

## Sicherheit

Der öffentliche Workflow ist absichtlich bereinigt:

- keine API-Schlüssel im Repository
- keine produktiven Credential-IDs
- keine gepinnten Formulardaten, IP-Adressen oder Test-Submissions

Für PageSpeed wird `PAGESPEED_API_KEY` als Umgebungsvariable erwartet. Externe Dienste und n8n-Credentials müssen nach dem Import neu verbunden werden.

## Hinweis

Dies ist ein Showcase der Automatisierungs- und Analysearchitektur. Ein produktiver Einsatz benötigt eigene Credentials, Datenschutzprüfung, Fehlerbehandlung und ein zum jeweiligen Projekt passendes Reporting.
