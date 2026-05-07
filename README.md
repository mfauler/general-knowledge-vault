# general-knowledge-vault

Öffentlicher Spiegel zentraler Konzeptdokumente aus Michaels Obsidian-Vault. Dient als URL-zugänglicher Kontext für Claude.ai (Web/Android), wo lokale MCP-Server nicht verfügbar sind.

## Struktur

```
general-knowledge-vault/
├── _KONTEXT.md       Konsolidierter Index + Essentials (Hauptdatei für Claude.ai)
├── README.md         Diese Übersicht
├── berufsbilder/     Berufsbilder MT-Familie, ATA, DA, SLT, Synthesen
├── sofl/             Störungsbildorientierte Funktionslehre
└── diagnostik/       Diagnostik-Ansätze, Funktionsorientierte Medizin
```

## Aktualisierung

Wird vom Slash-Command `/update-claude-web-context` aus Claude Code im lokalen Vault automatisch synchronisiert. Manuelle Bearbeitung wird vom nächsten Sync überschrieben.

## Zugriff durch Claude.ai

`_KONTEXT.md` wird per `web_fetch` aus Claude.ai-Projekten abgerufen. Volltexte sind über die Ordnerpfade ebenfalls per `web_fetch` zugänglich, etwa:

- https://raw.githubusercontent.com/mfauler/general-knowledge-vault/main/_KONTEXT.md
- https://raw.githubusercontent.com/mfauler/general-knowledge-vault/main/sofl/Trias%20der%20Befundkategorien.md

## Hinweis

Repository ist absichtlich öffentlich (Voraussetzung für `web_fetch` ohne Authentifizierung). Inhalte sind didaktisch-konzeptionell, ohne Patientendaten oder andere sensible Informationen.
