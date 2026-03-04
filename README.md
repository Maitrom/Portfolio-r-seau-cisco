#  Portfolio Réseau : Configuration Initiale & Protocoles

Ce dépôt documente mon apprentissage pratique issu du cours **Cisco Networking Academy : Networking Devices and Initial Configuration**

**Objectif :** Apprendre les éléments essentiels des périphériques réseau et la façon de les configurer pour ensuite pouvoir être capable de créer un petit réseau cisco

---
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

### Lab 2 : Configuration de base d'un routeur
* **Contexte :** Effectuer les tâches de configuration de base d'un router.
* **Actions réalisées :**
  * Accédez au mode privilégié et examiner la configuration actuelle en entrant les commandes ; 'enable', 'show running-config'
  * Configurer et vérifier la configuration initiale du routeur en utilisant les commandes ; 'hostname R1', 'enable secret itsasecret', 'line console 0 - password letmein - login - exit'
  * Encrypter les mots de passe en utilisant la commande 'service password-encryption'
  * Configurer un message légal en utilisant '# banner motd #L'accès non authorisé est strictement interdit#'
* **Résultat :** Après avoir utiliser 'show startup-config' j'ai pu confirmer que la configuration a bien été prise en comtpe.
*  **Preuve :** <img width="1052" height="500" alt="configuration-d-un-routeur" src="https://github.com/user-attachments/assets/a45d49ac-9990-462f-9737-764debb02004" />


### Lab 3 : [Ajoute ton prochain gros projet ici]
* **Contexte :** (Ex: Configuration du routage entre deux réseaux distincts).
* **Actions réalisées :** ...
* **Résultat :** ...

---

##  Ma Démarche d'Apprentissage
Je ne me contente pas de suivre des tutoriels : je cherche à comprendre le *pourquoi*. Par exemple, comprendre comment les paquets sont formatés (comme les fins de ligne en FTP) me permet d'anticiper les erreurs de configuration sur des infrastructures hétérogènes.

---
*N'hésitez pas à me contacter via [Mon LinkedIn](Lien_vers_ton_profil) pour échanger sur ces sujets !*
