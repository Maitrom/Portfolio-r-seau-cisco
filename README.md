#  Portfolio Réseau : Configuration Initiale & Protocoles

Ce dépôt documente mon apprentissage pratique issu du cours **Cisco Networking Academy : Networking Devices and Initial Configuration**

**Objectif :** Apprendre les éléments essentiels des périphériques réseau et la façon de les configurer pour ensuite pouvoir être capable de créer un petit réseau cisco

---

##  Journal des Laboratoires Pratiques

### Lab 1 : Effectuer la configuration de base d'un commutateur (switch)
* **Contexte :** Mise en place d'un nouveau switch dans un environnement d'entreprise.
* **Actions réalisées :**
  * Utilisation de la CLI du commutateur
  * Passer en mode privilégié en utilisant la commande 'enable' puis 'configure terminal' pour passer en configuration globale.
  * Configuration d'un nom d'hôte en utilisant la command 'hostname _nom d'hôte_
  * Configuration d'une addresse ip pour la SVI en utilisant les commandes ; 'interface vlan 1', 'ip address _addresse ip assignée_', 'no shutdown'
  * Quitter le mode de configuration globale et enregister la configuration en utilisant respectivement ; 'end', 'copy running-config startup-config'
  * Vérification de la configuration de l'addresse ip en utilisant 'show ip interface brief' et vérifier dans la table si la configuration est ok
* **Résultat :** La table me confirme bien que l'addresse ip a bien été assignée.
* **Preuve :** <img width="755" height="674" alt="configuration-switch" src="https://github.com/user-attachments/assets/c02e5835-cfda-409f-8db9-c3a5a52de841" />

### Lab 2 : Configuration de base d'un routeur
* **Contexte :** Effectuer les tâches de configuration de base d'un router.
* **Actions réalisées :**
  * Accéder au mode privilégié et examiner la configuration actuelle en entrant les commandes ; 'enable', 'show running-config'
  * Configurer et vérifier la configuration initiale du routeur en utilisant les commandes ; 'hostname R1', 'enable secret itsasecret', 'line console 0 - password letmein - login - exit'
  * Chiffrer les mots de passe en utilisant la commande 'service password-encryption'
  * Configurer un message légal en utilisant '# banner motd #L'accès non autorisé est strictement interdit#'
* **Résultat :** Après avoir utilisé 'show startup-config' j'ai pu confirmer que la configuration a bien été prise en comtpe.
*  **Preuve :** <img width="1052" height="500" alt="configuration-d-un-routeur" src="https://github.com/user-attachments/assets/a45d49ac-9990-462f-9737-764debb02004" />


### Lab 3 : Configurer SSH
* **Contexte :** Sécurisation d'un commutateur distant avec le cryptage du mot de passe SSH.
* **Actions réalisées :** ...
* Etablir une connexion telnet vers S1 en utilisant'telnet 10.10.10.2'
* Enregistrer la configuration actuelle de sorte que toutes les éventuelles erreurs commises soient annulées en basculant l'interrupter de S1
* Basculer dans le mode de configuration global pour ensuite chiffrer les mots de passe ; 'configure terminal' - 'service password-encryption'
* Définir le nom de domaine sur netacad.pka ; 'ip domain-name netacad.pka'
* Générer les clés RSA en spécifiant une longueur de 1024 bits ; 'crypto key generate rsa'
* Créer un utilisateur SSH et reconfigurer les lignes VTY pour un accès SSH uniquement ; 'line vty 0 15' - 'login local' - 'transport input ssh' - 'no password cisco'
* **Résultat :** Après avoir quitter la session Telnet, il m'était impossible de m'y reconnecter de cette manière. J'ai bien pu ne m'y reconnecter que grâce à la commande 'ssh -l administrator 10.10.10.2'
 <img width="893" height="545" alt="configurer-ssh" src="https://github.com/user-attachments/assets/742e1a54-3e26-4030-abeb-6011872a208e" />


### Lab 4 : Construire un réseau de commutateurs et de routeurs en utilisant la théorie vue précédemment
* **Contexte :**  Votre travail consiste à connecter les appareils, à mettre en œuvre une configuration de base et à vérifier la connectivité. Après avoir vérifié la connectivité du réseau, vous utiliserez les commandes IOS pour récupérer des informations sur les périphériques afin de répondre aux questions concernant votre équipement réseau. Vous allez également configurer le routeur pour un accès à distance sécurisé.
* **Actions réalisées :**
  *Connecter R1 G0/0/1 à n'importe quel port sur S1 avec un cable droit en cuivre
  * Connecter PCa à n'importe quel port sur S1
  * Connecter PCB à R1 G0/0/0
  * Configurer les paramètres de l'addresse IPv4, du masque de sous-réseau et de la passerelle par défaut PCA et ud PCB en utilisant la table d'addressage
  * On utilise la commande 'ping' entre les deux PC mais celle-ci échoue puisque le routeur n'a pas encore été configuré
  * Pour R1, attribuer un nom d'hôte en fonction de la table d'adressage, attribuer class comme mot de passe crypté EXEC privilégié, attribuer cisco comme mot de passe console. Chiffrer les mots de passe
  * <img width="454" height="166" alt="Configuration-routeur-R1" src="https://github.com/user-attachments/assets/8e4d9770-594b-4c15-931a-1e67aaa009be" />
  * Pour G0/0/0 et G0/0/1, configurer l'adressage IP selon la table et activez l'interface
  * <img width="696" height="247" alt="configurer-G01" src="https://github.com/user-attachments/assets/3b2207f8-fc09-4c19-a2c4-be2270255985" />
  * Pour S1, on attribue un nom d'hôte, un mot de passe crypté EXEC privilégié, un mot de passe console, et utiliser la commande 'service password-encryption' pour chiffrer les mots de passe
  * Pour VLAN 1, on configure l'addressage IP selon la table, on configure la passerelle par défaut et on enregistre la configuration courante de le fichier de démarrage.
  * <img width="633" height="431" alt="configurer-S1" src="https://github.com/user-attachments/assets/d9436dc4-d647-4d74-8a70-99b8ed879ac6" />
  * Sur R1, configurer le nom de domaine academy.net et générer des clés RSA avec une longueur de clé de 1024.
  * Créer un utilisateur avec SSHuser comme nom d'uilisateur et cisco comme mot de passe
  * Configurer les lignes VTY
  * <img width="527" height="243" alt="R1-config-ssh" src="https://github.com/user-attachments/assets/de33a9dc-ee81-4c45-bba1-1ea901ba381d" />
  * <img width="743" height="256" alt="addressage-table" src="https://github.com/user-attachments/assets/1462feb0-29e3-4c6d-9979-021f85a68d0b" />
  * <img width="606" height="151" alt="architecture" src="https://github.com/user-attachments/assets/0b15d88b-554a-4f4b-83f3-289e76f58ae0" />



* **Résultat :**
* Connectivité validée entre PCA et PCB confirmée par les tests de ping réussis entre ceux-ci.
* Validation du message légal ; la bannière MOTD s'affiche correctement dès la tentative de connexion.
<img width="271" height="146" alt="connexionssh" src="https://github.com/user-attachments/assets/ed2510f2-dcdc-46f8-871f-1a1702a5170b" />



