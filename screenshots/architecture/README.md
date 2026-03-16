# Architecture du SOC Homelab

Ce dossier contient les captures d’écran de l’architecture de mon laboratoire SOC.

## Infrastructure

Le lab est hébergé sur VMware ESXi et contient les machines suivantes :

- DC01 – Windows Server 2022 – Domain Controller
- DC02 – Windows Server 2022 – Domain Controller
- MYSQL – Ubuntu 22.04 – Serveur base de données
- MAIL – Ubuntu 22.04 – Serveur mail
- ZABBIX – Ubuntu 22.04 – Serveur monitoring
- GLPI – Ubuntu 22.04 – Gestion de parc informatique
- DHCP – Ubuntu 22.04 – Serveur DHCP
- WAZUH – Ubuntu 22.04 – SIEM Manager

## Objectif

Cette architecture permet de simuler un environnement d’entreprise pour :

- la détection d’attaques
- la supervision de sécurité
- l’analyse SOC
- l’utilisation d’un SIEM (Wazuh)

## Contenu du dossier

- diagramme de l’architecture
- vue réseau du lab
- machines virtuelles du SOC homelab
