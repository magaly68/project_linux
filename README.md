# projet linux

Ce projet contient:
- un document sur le modèle OSI
- il contient un tp linux et le rapport qui lui est associé
- il contient aussi mon premier projet perso en C 

Rapport de TP – Administration Linux (SSH et SCP)

Introduction

L’objectif de ce TP est  de mettre en pratique les bases de l’administration réseau sous Linux à travers l’installation et la configuration de services sur des machines virtuelles. 
il s’agissait plus précisément de :

- Installer et configurer OpenSSH pour permettre la connexion distante entre deux machines virtuelles Debian.
- Utiliser la commande SCP pour transférer des fichiers entre les deux machines.
- Découvrir et appliquer des commandes Linux essentielles pour manipuler le système.

Ce TP avait également pour but de comprendre les mécanismes de communication client/serveur sous Linux et de se familiariser avec la résolution de problèmes liés aux services réseau.

1.Matériel et environnement

- Deux machines virtuelles (VM1 et VM2) sous Debian.
- 8 Go de RAM sur la machine hôte.
- Interfaces graphiques : tentative avec GNOME puis installation de XFCE pour plus de légèreté.
- Services installés : openssh-server.
- Outils utilisés : terminal, éditeur nano, commandes ssh, scp, systemctl, ip a, cat, ls...

2.Méthodologie et étapes réalisées

- Installation et configuration SSH
- Installation du paquet openssh-server sur la VM2.
- Vérification de l’état du service avec la commande systemctl status ssh
- Modification et vérification du fichier /etc/ssh/sshd_config
- Connexion SSH:
  - Tentative de connexion depuis la VM1 vers la VM2 avec la commande ssh utilisateur@ip_vm2
  - Blocage rencontré : connection refused.
- Vérification de l’IP avec ip a et des ports ouverts.
- Transfert de fichiers avec SCP: 
 
Commande testée : scp home/user/Documents/fichiersXML la commande a échoué plusieurs fois, après avoir fait la commande whoami j'ai pu voir que le dossier user s'appelait...magaly, ce qui a changé beaucoup de chose mais ça n'a pas réglé le problème pour autant.

Les difficultés que j'ai rencontrées sont essentiellement des difficultés matérielles et de fonctionnement (j'ai eu des soucis avec mon pc ce qui m'a fait prendre du retard par rapport aux autres membres du groupe, j'ai aussi du désinstaller et réinstaller plusieurs fois les vm parce qu'elle ne fonctionnaient pas 

3.Résultats
L’installation d’OpenSSH a été réalisée avec succès mais les tests de connexion SSH n’ont pas fonctionné correctement (erreurs connection refused).
Le service SSH était pourtant lancé, ce qui montre que le problème venait probablement de la configuration réseau ou du firewall donc j'ai pas trop compris. La commande scp n’a pas pu être validée à cause du même problème.
En revanche, les commandes de base (affichage de fichiers, recherche de scripts .sh, utilisation des variables d’environnement comme $PWD et $IFS) ont fonctionné correctement.

4.Analyse et discussion

Ce TP m'a permis d'apprendre à travailler avec l'environnement Linux et de voir qu'on peut travailler uniquement avec le terminal contrairement à ce que penser avec Windows. 
Il m'a aussi permis de:
Comprendre le rôle des services et des fichiers de configuration.
Savoir diagnostiquer une panne (exemple : service actif mais port non accessible).
Travailler avec la configuration réseau entre deux VM.
Les erreurs rencontrées (crash VM, clavier incorrect, connexion SSH impossible) ont ralenti la progression, mais elles ont été instructives car elles obligent à chercher les causes (réseau, permissions, service, pare-feu).

Conclusion

Ce TP m’a permis de découvrir comment installer SSH sous Debian mais aussi comment utiliser la commande SCP pour copier des fichiers à distance, ce que je ne savais pas faire avant et d'ailleurs je savais pas que c'était possible.
J'ai aussi pu voir quelles sont les difficultés fréquentes liées à la configuration réseau et aux services sous Linux.
Même si certaines étapes n’ont pas abouti, j’ai mieux compris le fonctionnement de SSH et les méthodes pour diagnostiquer une connexion refusée.





