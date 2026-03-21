# SOC Homelab - Wazuh

## Présentation

Ce projet présente la mise en place d’un laboratoire SOC (Security Operations Center) personnel.

L’objectif est de simuler un environnement d’entreprise afin de surveiller les événements de sécurité, détecter des attaques et analyser les incidents à l’aide du SIEM Wazuh.

---

## Infrastructure du laboratoire

Le lab est hébergé sur VMware ESXi et contient les machines suivantes :

- DC01 – Windows Server 2022 – Domain Controller
- DC02 – Windows Server 2022 – Domain Controller
- MYSQL – Ubuntu 22.04 – Serveur base de données
- MAIL – Ubuntu 22.04 – Serveur mail
- ZABBIX – Ubuntu 22.04 – Serveur monitoring
- GLPI – Ubuntu 22.04 – Gestion de parc informatique
- DHCP – Ubuntu 22.04 – Serveur DHCP
- WAZUH – Ubuntu 22.04 – SIEM Manager

---

## Architecture du laboratoire

![Architecture](screenshots/architecture/network-topology.png)

---

## Wazuh Dashboard

![Dashboard](wazuh-dashboard.png)

---

## Simulation d’attaque – SSH Brute Force

### Scénario

Une attaque brute force SSH a été simulée sur un serveur Linux afin de tester la détection du SIEM Wazuh.

### Détection

Wazuh a détecté :

- plusieurs tentatives de connexion échouées
- des utilisateurs invalides
- une activité anormale

### MITRE ATT&CK

- T1110 – Brute Force

### Preuve

![Bruteforce](screenshots/architecture/ssh_brute_force_detection.png)

### Analyse

Les logs montrent des tentatives répétées de connexion SSH.

Wazuh a correctement généré des alertes correspondant à une attaque brute force.

### Conclusion

Le SIEM permet de détecter efficacement ce type d’attaque en temps réel.

---

## Compétences démontrées

- Déploiement SIEM (Wazuh)
- Analyse de logs
- Détection d’attaques
- Utilisation MITRE ATT&CK
- Investigation SOC
