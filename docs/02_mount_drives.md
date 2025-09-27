# Schritt 2 – Festplatten einbinden

Dieses Dokument beschreibt das Einbinden der beiden 4 TB Festplatten in das Dateisystem des Raspberry Pi.  
Ziel: Die Laufwerke sollen beim Start automatisch unter `/srv/samba/share1` und `/srv/samba/share2` verfügbar sein.

---

## Laufwerke identifizieren

Auf dem Pi ausführen:
```bash
lsblk -o NAME,SIZE,FSTYPE,MOUNTPOINT,UUID

## fstab bearbeiten

Damit die beiden 4 TB Festplatten beim Start automatisch eingebunden werden, 
müssen die Mountpoints in der Datei `/etc/fstab` eingetragen werden.

1. Datei öffnen:
   ```bash
   sudo nano /etc/fstab

2. Diese Zeilen am Ende der Datei eintragen:

UUID=6C9B-F31D   /srv/samba/share1   exfat   defaults,uid=pi,gid=pi   0   0
UUID=69FF-EE7B   /srv/samba/share2   exfat   defaults,uid=pi,gid=pi   0   0

3. Speichern und Beenden:  
- **Ctrl + O** → Enter  
- **Ctrl + X**

4. Änderungen testen:
```bash
sudo mount -a
lsblk -o NAME,SIZE,FSTYPE,MOUNTPOINT
