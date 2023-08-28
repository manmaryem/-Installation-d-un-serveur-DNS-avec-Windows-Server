# -Installation-d-un-serveur-DNS-avec-Windows-Server

## Étape 1: Installation du serveur DNS
- Ouvrez le Gestionnaire de serveur.Cliquez sur "Gérer" dans le coin supérieur droit, puis sélectionnez "Ajouter des rôles et des fonctionnalités".
Suivez l'assistant d'ajout de rôles jusqu'à la section "Sélection des rôles du serveur".
Cochez la case "Serveur DNS", puis suivez les étapes pour terminer l'installation.
![image](https://github.com/manmaryem/-Installation-d-un-serveur-DNS-avec-Windows-Server/assets/137881827/a51b549e-9d33-469c-82e3-d6ea5da12c07)

![image](https://github.com/manmaryem/-Installation-d-un-serveur-DNS-avec-Windows-Server/assets/137881827/ca0b251a-e3e0-4887-bd88-9d5013e31e71)

## Étape 2: Configuration du serveur DNS
Ouvrez la console "Gestionnaire DNS" à partir du menu "Outils d'administration".
- changement du nom du serveur a partire du server local
- 
  ![image](https://github.com/manmaryem/-Installation-d-un-serveur-DNS-avec-Windows-Server/assets/137881827/297d2b3d-718f-40d4-9888-7f4e62191436)

![image](https://github.com/manmaryem/-Installation-d-un-serveur-DNS-avec-Windows-Server/assets/137881827/08dbda3c-e336-4fe8-bf78-a30a4dffb724)

Cliquez avec le bouton droit sur votre serveur dans la console DNS, puis sélectionnez "Nouvelle zone de domaine".
Suivez l'assistant pour créer une nouvelle zone principale avec le nom "winder.lan".
![image](https://github.com/manmaryem/-Installation-d-un-serveur-DNS-avec-Windows-Server/assets/137881827/bfdee553-70eb-43d7-b2a8-87e9a64bc513)

## Étape 3: Configuration des enregistrements DNS
- Enregistrements du Hote (AAA)
Sous la zone "wilders.lan", cliquez avec le bouton droit, puis sélectionnez "Nouvel enregistrement hôte (A ou AAAA)".
Entrez "serveur" comme nom d'hôte et entrez l'adresse IP du serveur.
Répétez les étapes pour ajouter un enregistrement A pour la machine avec une réservation IP fixe, dans mon exemple "PC" avec son adresse IP.

![image](https://github.com/manmaryem/-Installation-d-un-serveur-DNS-avec-Windows-Server/assets/137881827/c626c305-7681-4934-ab8d-8d18173e71ba)

- Enregistrement CNAME
Sous la zone "wilders.lan", cliquez avec le bouton droit, puis sélectionnez "Nouvel enregistrement Alias (CNAME)".
Entrez "dns" comme nom d'hôte Alias

![image](https://github.com/manmaryem/-Installation-d-un-serveur-DNS-avec-Windows-Server/assets/137881827/9cabc134-a8fd-4293-8e99-709514720617)

## Étape 4: Configuration de la zone de recherche inversée
Dans  "Gestionnaire DNS".
Sous le serveur DNS, cliquez avec le bouton droit, puis sélectionnez "Nouvelle zone de recherche inversée".
Suivez l'assistant pour créer une nouvelle zone de recherche inversée.
Choisissez la classe d'adresse IP appropriée (généralement IPv4).
Sélectionnez la plage d'adresses IP à couvrir par la zone de recherche inversée.
cliquez avec le bouton droit, puis sélectionnez "Nouvel enregistrement PTR".
Entrez le dernier octet de l'adresse IP sous forme numérique mon adresse IP 192.168.1.10
Entrez le nom complet du serveur correspondant à cette adresse IP "serveur.winder.lan".

![image](https://github.com/manmaryem/-Installation-d-un-serveur-DNS-avec-Windows-Server/assets/137881827/3137fd89-a0f6-4798-bd48-5cb0318906db)

## Étape 5: Vérification et tests

![image](https://github.com/manmaryem/-Installation-d-un-serveur-DNS-avec-Windows-Server/assets/137881827/958c3470-a76b-4cde-b8c3-5b6f83d32a16)


![image](https://github.com/manmaryem/-Installation-d-un-serveur-DNS-avec-Windows-Server/assets/137881827/6db08fbe-2b77-43ed-9e73-13b3d2315c16)










