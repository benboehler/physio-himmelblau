# Physio Himmelblau

Dies ist das Repository für die Physio Himmelblau Website, erstellt mit Astro.

## 🚀 Projektstruktur

Innerhalb deines Astro-Projekts findest du folgende Ordner und Dateien:

```text
/
├── public/
│   └── favicon.svg
├── src
│   ├── assets
│   │   └── astro.svg
│   ├── components
│   │   └── Welcome.astro
│   ├── layouts
│   │   └── Layout.astro
│   └── pages
│       └── index.astro
├── package.json
└── deploy.txt
```

## 🧞 Befehle

Alle Befehle werden aus dem Stammverzeichnis des Projekts über das Terminal ausgeführt:

| Befehl            | Aktion                                           |
| :---------------- | :----------------------------------------------- |
| `pnpm install`    | Installiert die Abhängigkeiten                  |
| `pnpm dev`        | Startet den lokalen Dev-Server (localhost:4321)  |
| `pnpm build`      | Erstellt die Produktionsseite in `./dist/`      |
| `pnpm deploy`     | **Baut die Seite und lädt sie zu Hostpoint hoch** |
| `pnpm preview`    | Lokale Vorschau des Builds                      |

## 📦 Deployment (Hostpoint)

Das Deployment erfolgt automatisiert via WinSCP.

### Voraussetzungen
Um das Deployment von deinem Rechner aus zu starten, müssen folgende Bedingungen erfüllt sein:

1.  **WinSCP**: Muss installiert sein (Standardpfad: `C:\Program Files (x86)\WinSCP`).
2.  **SSH Key**: Dein privater Schlüssel (`id_ed25519`) muss im Ordner `%USERPROFILE%\.ssh\` liegen.
3.  **Zugriff**: Dein öffentlicher Schlüssel muss im Hostpoint Control Panel hinterlegt sein.

### Ausführung
```sh
pnpm deploy
```
Dieser Befehl führt zuerst `pnpm build` aus und startet anschließend das WinSCP-Skript (`deploy.txt`), welches die Dateien auf den Server überträgt.

## 👀 Dokumentation

Weitere Informationen zu Astro findest du in der [offiziellen Dokumentation](https://docs.astro.build).
