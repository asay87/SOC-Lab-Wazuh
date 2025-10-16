# 🧩 Installation du Lab SOC - Wazuh

## 1. Environnement
- **Serveur** : Ubuntu 22.04 LTS (VM)
- **Client** : Windows 10 (VM)
- **Réseau** : NAT avec IP fixe (Ubuntu : 192.168.56.10 / Windows : 192.168.56.11)

---

## 2. Installation du serveur Wazuh

```bash
sudo apt update && sudo apt upgrade -y
sudo apt install curl vim net-tools ufw -y
sudo apt install curl apt-transport-https lsb-release gnupg -y

Active le pare-feu UFW :
sudo ufw allow ssh
sudo ufw enable
sudo ufw status
sudo chmod 600 /etc/netplan/01-netcfg.yaml

curl -sO https://packages.wazuh.com/4.13/wazuh-install.sh
curl -sO https://packages.wazuh.com/4.7/wazuh-install.sh
sudo bash ./wazuh-install.sh -a
```
On Verifie l'installation avec : 
```
sudo systemctl status wazuh-manager
sudo systemctl status wazuh-indexer
sudo systemctl status wazuh-dashboard
```
## 3. Installation de l’agent Windows
 B Windows 10
- Telechargement et installation du package d'installation 
  
