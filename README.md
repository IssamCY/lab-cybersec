# Lab Cybersécurité Personnel

## Objectif
Monter un environnement de test sur VM Ubuntu.

## Outils utilisés
- Nmap : scan et cartographie réseau
- Wireshark : analyse de trafic réseau
- Apache2 : serveur web cible pour les tests
- Lynis : audit de sécurité système

## Ce que j'ai fait

### 1. Scan réseau avec Nmap
- Scanné le réseau local 10.0.2.0/24
- Détecté 2 machines : la passerelle (10.0.2.2) et un serveur DNS dnsmasq (10.0.2.3)
- Installé Apache2 et détecté le port 80 ouvert avec la version du serveur

### 2. Analyse de trafic avec Wireshark
- Capturé du trafic DNS et HTTP en temps réel
- Observé les requêtes DNS vers le serveur 10.0.2.3 détecté avec Nmap

### 3. Audit de sécurité avec Lynis
- Score initial : 66/100
- Correction 1 : activation du pare-feu UFW → 67/100
- Correction 2 : installation de fail2ban → 69/100
- Correction 3 : mises à jour automatiques de sécurité

## Ce que j'ai appris
- Comment cartographier un réseau et identifier les services exposés
- L'importance de filtrer le trafic réseau pour détecter des anomalies
- Comment auditer et durcir un système Linux

