# Playbooks für proxmox repositiories und update sowie sdn vorbereiten und ein paar tools installieren.
Sammlung von Playbooks um einen Proxmox-Server nach der Installation upzudaten und für SDN vorzubereiten.
Benötigt wird ein python venv und ansible.

Dazu bitte requirements.txt installieren.

## 1_proxy.yml
Falls der Proxmox einen Proxy benötigt, trage ihn im Inventory ein und führe 1_proxy.yml vor den anderen Playbooks aus

## 2_proxmox-update.yml
Das Proxmox Community-Repo wird konfiguriert und Updates installiert.
Der Hinweis, dass man keine lizensierte Version betreibt wird nicht entfernt.

## 3_sdn-prerequisites.yml
Die Voraussetzungen für SDN werden installiert.
Falls man eine lokale Installation mit Jumboframes betreibt kann man die MTU dafür im Playbook einstellen.

Einige weitere sinnvolle Pakete (totally meine eigene Meinung) werden auch installiert, die Liste kann nach Belieben angepasst werden.

## optional (wenn virtualisiert)
install-qemu-guest-agent.yml installiert den qemu-guest-agent falls der Server virtualisiert ist.

... und natürlich das inventory.yml wo die zu bearbeitenden hosts drin stehen.