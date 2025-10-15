# 🧩 Installation du Lab SOC - Wazuh

## 1. Environnement
- **Serveur** : Ubuntu 22.04 LTS (VM)
- **Client** : Windows 10 (VM)
- **Réseau** : NAT avec IP fixe (Ubuntu : 192.168.56.10 / Windows : 192.168.56.11)

---

## 2. Installation du serveur Wazuh

```bash
sudo apt update && sudo apt upgrade -y
curl -sO https://packages.wazuh.com/4.7/wazuh-install.sh
sudo bash ./wazuh-install.sh -a
```
## 3. Installation de l’agent Windows
 B Windows 10
- Telechargement et installation du package d'installation 
  
