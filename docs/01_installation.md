# Schritt 1 – Samba Server Installation (Neuaufbau)

Dieses Dokument beschreibt die Neuinstallation von Samba auf dem Raspberry Pi 3.  
Alle Schritte werden vom **Mac Mini** aus durchgeführt (SSH-Verbindung).  
Der **Windows-Laptop (Schule)** soll später ohne Adminrechte auf den Server zugreifen können (lesen & schreiben).

---

## Voraussetzungen

- Raspberry Pi 3 mit Raspberry Pi OS (aktuell)
- SSH-Zugang vom Mac Mini
- Zwei 4 TB HDDs angeschlossen am Pi
- Internetverbindung für Paketinstallation

---

## Vorbereitung

1. Mit dem Raspberry Pi verbinden (ausführen **auf dem Mac Mini**):
   ```bash
   ssh pi@raspiserver.local

---

## Installation

1. Samba installieren (ausführen **auf dem Pi**):
   ```bash
   sudo apt install samba samba-common-bin -y

2. Version prüfen (ausführen **auf dem Pi**):
   ```bash
   smbd --version

---

