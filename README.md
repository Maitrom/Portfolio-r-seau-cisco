#  Portfolio Réseau : Configuration Initiale & Protocoles

Ce dépôt documente mon apprentissage pratique issu du cours **Cisco Networking Academy : Networking Devices and Initial Configuration**

**Objectif :** Apprendre les éléments essentiels des périphériques réseau et la façon de les configurer pour ensuite pouvoir être capable de créer un petit réseau cisco

---

##  Compétences Techniques Acquises

| Catégorie | Compétences & Technologies |
| :--- | :--- |
| **Fondamentaux** | Modèles OSI & TCP/IP, Adressage IPv4/IPv6, Subnetting |
| **Équipements** | Commutateurs (Switches) Cisco (Séries 2960, 4000) |
| **Protocoles** | 
| **Outils** | Cisco Packet Tracer|

---

##  Journal des Laboratoires Pratiques

### Lab 1 : Effectuer la configuration de base d'un commutateur (switch)
* **Contexte :** Mise en place d'un nouveau switch dans un environnement d'entreprise.
* **Actions réalisées :**
  * Utilisation de la CLI du commutateur
  * Passer en mode privilégier en utilisant la commande 'enable' puis 'configure terminal' pour passer en configuration globale.
  * Configuration d'un nom d'hôte en utilisant la command 'hostname _nom d'hôte_
  * Configuration d'une addresse ip pour la SVI en utilisant les commandes ; 'interface vlan 1', 'ip address _addresse ip assignée_', 'no shutdown'
  * Quitter le mode de configuration globale et enregister la configuration en utilisant respectivement ; 'end', 'copy running-config startup-config'
  * Vérification de la configuration de l'addresse ip en utilisant 'show ip address brief' et vérifier dans la table si la configuration est ok
* **Résultat :** La table me confirme bien que l'addresse ip a bien été assignée.
* **Preuve :** <img width="755" height="674" alt="configuration-switch" src="https://github.com/user-attachments/assets/c02e5835-cfda-409f-8db9-c3a5a52de841" />

### Lab 2 : Analyse des Protocoles de Transfert (FTP & Telnet)
* **Contexte :** Module de cybersécurité (TryHackMe) sur l'utilisation et la sécurisation des protocoles non chiffrés.
* **Actions réalisées :**
  * Interception et analyse de trafic Telnet pour démontrer la vulnérabilité des mots de passe en clair.
  * Utilisation du protocole FTP en ligne de commande pour la récupération de fichiers.
  * **Analyse technique :** Différenciation et application des modes de transfert FTP (`ASCII` vs `Binary`). J'ai documenté l'importance du mode ASCII pour la traduction correcte des sauts de ligne (LF vs CR+LF) entre les environnements Linux et Windows, garantissant ainsi l'intégrité des scripts récupérés.
* **Résultat :** Maîtrise des interactions client-serveur via des terminaux bruts.

### Lab 3 : [Ajoute ton prochain gros projet ici]
* **Contexte :** (Ex: Configuration du routage entre deux réseaux distincts).
* **Actions réalisées :** ...
* **Résultat :** ...

---

##  Ma Démarche d'Apprentissage
Je ne me contente pas de suivre des tutoriels : je cherche à comprendre le *pourquoi*. Par exemple, comprendre comment les paquets sont formatés (comme les fins de ligne en FTP) me permet d'anticiper les erreurs de configuration sur des infrastructures hétérogènes.

---
*N'hésitez pas à me contacter via [Mon LinkedIn](Lien_vers_ton_profil) pour échanger sur ces sujets !*
