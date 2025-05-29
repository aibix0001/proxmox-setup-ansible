# Playbook für proxmox repositiories und update sowie sdn vorbereiten und ein paar tools installieren.
Playbook um einen Proxmox-Server nach der Installation upzudaten und für SDN vorzubereiten.
Benötigt wird ein Python venv und ansible.

Dazu bitte requirements.txt installieren.

## 1. Proxy
Falls der Proxmox einen Proxy benötigt, trage ihn im Inventory ein, ein Beispiel ist im inventory.yml.example

## 2. Proxmox Repo und Update
Das Proxmox Community-Repo wird konfiguriert und Updates installiert.
Der Hinweis, dass man keine lizensierte Version betreibt wird nicht entfernt.

## 3. SDN Vorbereitungen und diverse Pakete installieren
Die Voraussetzungen für SDN werden installiert.
Falls man eine lokale Installation mit Jumboframes betreibt kann man die MTU dafür im Inventory einstellen.

Einige weitere sinnvolle Pakete (totally meine eigene Meinung) werden auch installiert, die Liste kann nach Belieben angepasst werden.

## optional (wenn virtualisiert)
install-qemu-guest-agent.yml installiert den qemu-guest-agent falls der Server virtualisiert ist.

... und natürlich das inventory.yml wo die zu bearbeitenden hosts drin stehen.