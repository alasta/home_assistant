# Mon dashboard Unifi sur Home Assistant

## Pre-requis

- Avoir du matériel Unifi, ici un UDM
- Un home assistant fonctionnel
- Un HACS fonctionnel
- Créer un compte admin sur l'UDM 

## Mise en place des composants

Installer et configurer l'intégration **UniFi Network** disponible de base sous HA.  
Installer et configurer l'intégration dans HACS :  

  - **Sensor.Unifigateway** 
  - optionnellement **Custom brand icons** (pour des icones)
  - **mini-graph-card**
  - **card_mod**
  - **bar-card**


## Configuration

Le contenu du fichier **sensor.yaml** est à mettre dans votre **configuration.yaml** ou fichier YAML de configuration sensor.  
Il y a SSID01 à SSID04, c'est à modifier par vos SSID, j'en ai 4 pour mes besoins.  
Note: dans le yaml, pour les sensors **unifi_ssid_SSIDXX_count_device..** , il faut mettre le SSIDXX en minuscule sinon HA ne va pas les prendres, mais dans le reste de la configuration respecter les minuscules/majuscules du SSID. 
    
Dans le **dashboard.yaml** le contenu pour les dashboards (mettre l'image unifi sur le serveur HA et modifier l'IP de l'UDM pour le lien HTTPS).  
Il y en a un pour les infos Unifi et l'autre pour bloquer les accès réseaux.  

Note : le logo unifi est dans le dossier **assets** et le mettre dans le dossier HA : **/config/www/pics** (peut être à créer).
Modifier les entitées qui correspondent à vos machines, rechercher **switch.machineaaa**.

## Résultat
![Image1](./screenshots/01.png)



![Image2](./screenshots/02.png)

![Image3](./screenshots/03.png)
