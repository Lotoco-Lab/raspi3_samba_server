# Schritt 2 – Festplatten einbinden

Dieses Dokument beschreibt das Einbinden der beiden 4 TB Festplatten in das Dateisystem des Raspberry Pi.  
Ziel: Die Laufwerke sollen beim Start automatisch unter `/srv/samba/share1` und `/srv/samba/share2` verfügbar sein.

---

## Laufwerke identifizieren

Auf dem Pi ausführen:
```bash
lsblk -o NAME,SIZE,FSTYPE,MOUNTPOINT,UUID
