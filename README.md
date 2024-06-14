# checkpoint1

## EXERCICE 1:

Après avoir tapé la commande: lsblk pour vérifier les différents disques et leurs informations (Nom? taille?)
Il faut taper la commande "fdisk /dev/sdb" pour partitionner le disque 2.

<img width="663" alt="Capture d’écran 2024-06-14 à 09 29 15" src="https://github.com/bbrice28/checkpoint1/assets/169658100/a97a5cfa-6a35-430c-ba50-5244c6a65942">

Ensuite, je renomme les deux partitions "DATA" et "SWAP", et les configure en système de fichier "ext4" et "SWAP":

<img width="633" alt="Capture d’écran 2024-06-14 à 09 36 27" src="https://github.com/bbrice28/checkpoint1/assets/169658100/4e964f24-ee27-4334-99d7-d295e9743b9d">

Je récupère l'uuid de DATA avec la commande "blkid /dev/sdb1", et j'obtiens UUID="76fe6955-a38-497b-9222-0bb98061ea19".
Je vais ensuite modifier le fichier "fstab" pour monter la partition automatiquement au démarrage de la machine.
<img width="632" alt="Capture d’écran 2024-06-14 à 09 49 11" src="https://github.com/bbrice28/checkpoint1/assets/169658100/4bce1b0e-fe89-41bb-bfac-eed0a5305b66">

Enfin, je vais monter toutes les partitions inscrites dans le fichier "fstab" avec la commande "mount -a"
<img width="636" alt="Capture d’écran 2024-06-14 à 09 51 23" src="https://github.com/bbrice28/checkpoint1/assets/169658100/3ec66610-a8c4-4e63-be1d-9da21e020077">


## EXERCICE 2:

Je commence par créer le fichier script avec la commande: "touch addUsers.sh".
Puis, je vais dans le fichier pour taper mon script avec la commande "nano addUsers.sh".
Ma première ligne sera le shebang "#!/bin/bash".

Je tape ensuite le script suivant:

<img width="638" alt="Capture d’écran 2024-06-14 à 11 18 28" src="https://github.com/bbrice28/checkpoint1/assets/169658100/973c6395-9b43-4121-9243-459f1634a214">

NB: - J'ai supprimé les crochets pour le "if id" car le script me sortait un message d'erreur "opération attendue"
    - J'ai redirigé la sortie de ce "if id" en /dev/null pour que celle ci ne s'affiche pas à l'éxécution du script
  

Enfin, je teste toutes les possibilités du script:

<img width="640" alt="Capture d’écran 2024-06-14 à 11 18 10" src="https://github.com/bbrice28/checkpoint1/assets/169658100/adc6e101-b091-4b1e-952b-8e4a24dd9aa6">






## EXERCICE 3:

## 1
La commande est "cat /etc/passwd". Les utilisateurs étant dans le fichier "/etc/passwd", et la commande permettant de le lire "cat".
## 2
Il faut taper la command "chmod 744 myfile".
7 pour permettre au propriétaire d'avoir tous les droits.
4 pour permettre au groupe la lecture seule.
4 pour permettre aux autres la lecture seule
## 3
Il faut faire un "gitignore "
## 4
Il faut faire un "git merge" sans oublier après le "git commit" pour valider.
## 5
Si le texte est dans un fichier il faut faire "cat fichier.txt".
Sinon, on utilise la commande "echo" suivie du texte.
## 6
Puisque le gedit est la tache numéro 1, et que la commande permettant de mettre en avant plan la tache est "fg %x". 
Ici "fg" voulant dire "foreground" ou "avant-plan".
Il faut donc taper la commande "fg %1".
## 7
Sur la couche 2 (liaisons des données), nous trouvons: La carte réseau qui se trouve dans les IoT/Ordinateurs et qui leurs permet de communiquer grâce (entre autres) à leurs adresses MAC avec le second appareil, le switch.
Le switch permet de rediriger les paquets à envoyer ou donnés par le routeur, qui est présent sur la couche 3 (le réseau).
Le routeur est donc le lien entre 2 réseaux différents, leurs permettant l'échange de paquets.
## 8
cp= CopyItem
cd= cd
mkdir= New-ItemProperty
ls= Get-ChildItem
## 9
Dans la trame Ethernet, le payload (charge utile), est l'information que l'on souhaite communiquer. Plus précisémment, après encapsulage, un bout de cette information.
## 10
Les classes gaspillaient les adresses IP ( puisque nous attribuions des classes fixes, certains réseaux avaient trop d'adresses ip, d'autres trop peu). Le CIDR permet d'optimiser les adressages, et ainsi de ralentir la pénurie d'IPV4.
