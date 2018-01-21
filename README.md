# Linux Search Engine Optimisation
L'objectif de cette machine virtuelle est de centraliser et partager des outils pour le référencement et le SEO.

# SEO Kalamity - Version 0.4
Télécharger l'image .ova avec ce lien pour soutenir le projet SEO Kalamity : https://cnhv.co/1cyiu

# Utilisateurs de la machine virtuelle
seo : UtilisateurSEO<br/>
root : OptimisationSEO

# Lien miroir
Télécharger l'image .ova en version 0.3 depuis Onedrive - https://onedrive.live.com -> https://1drv.ms/u/s!AqtUsyUfGwC9hEZZZdnDSLZiARBM<br/>
Télécharger l'image .ova en version 0.4 depuis MediaFire - https://www.mediafire.com -> http://www.mediafire.com/file/suef98dg7oj9dhs/SEO.ova

# Importer la machine virtuelle avec VirtualBox
Double cliquer sur l'archive .ova téléchargée pour importer la machine virtuelle Linux Search Engine Optimisation.<br/>
La version courante de SEO Kalamity sera ajoutée à VirtualBox.

# Démarrer et utiliser la machine virtuelle Linux Search Engine Optimisation
## Cours et prises de notes
Ajout de cours et prises notes dans le dossier /home/seo/DOCU-SEO/<br/>
Consulter les fichiers suivant : "SEO - Visuel.odg" et "SEO - Prise de notes.odt"

## Exemples disponibles
Ajout d'un exemple de masterspin dans /home/seo/DOCU-SEO/Tutoriels/Master spin/

## Logiciels installés
### Configurer Firefox
Sauvegarde des favoris de firefox dans le dossier /home/seo/DOCU-SEO/Sauvegarde/Les favoris de Firefox/<br/>
Le compte Firefox administrateur pour conserver la liste des favori est déconnecté lors du partage de la machine virtuelle.<br/>
Créer votre propre compte Firefox pour sauvegarder et syncroniser la liste des favoris actuelle et vos nouveaux favoris.

Le plugin Linkchecker est intégré pour vérifier si les liens de votre site ne sont pas brisés.<br/>
Le plugin PurTraqueur de PurMedia est intégré pour partager vos pages intéressantes en un clic sur PurMedia.
### Eclipse
L'outil de développement web Eclipse est disponible depuis le bureau.
### Mantra
L'outil navigateur pentest Mantra est disponible depuis le bureau.

## Scripts installés
### Gephi
L'outil Gephi est disponible depuis les scripts à partir du bureau.<br/>
La page Gephi sur le wiki est ajoutée dans les favoris du navigateur Firefox : https://www.visionduweb.eu/wiki/index.php?title=Accueil_SEO#Gephi
### Sitemap-e
Sitemap-e permet de créer un fichier sitemap.xml
### Minergate et la monnaie numérique
Créer un compte sur Minergate pour fabriquer de la monnaie numérique : https://minergate.com/a/8ac23bd407f9b6db4d848765<br/>
Installation du Mineur cpuminer pour aider les nouveaux utilisateurs de monnaie numérique (https://www.visionduweb.eu/wiki/index.php?title=Sites_gratuits_pour_gagner_du_Monero_depuis_votre_navigateur#Installer_le_mineur_cpuminer_sur_Debian_Stretch)
### Ping google bing sitemap
Ajout d'URL qui permettent de soumettre un fichier sitemap.xml par ping, aux moteurs de recherche.<br/>
/home/seo/Scripts/ping-google-bing-sitemap.sh

## Utiliser Docker et l'image lamp mysql PHP5 cURL
### Mise en place du serveur PHP lamp via Docker : docker pull tutum/lamp
Démarrer lamp : docker run -d -p 80:80 -p 3306:3306 tutum/lamp<br/>
Tutoriel Docker : https://www.visionduweb.eu/wiki/index.php?title=Ajouter_Docker_sur_GNU_Linux#Installer_une_image_Docker_lamp

### Importer l'image de Docker à neuf automatiquement
Réimporter l'image Docker avec Lamp MySQL PHP5 cURL : docker load -i /home/seo/IMAGE.tar<br/>

### Se connecter à une image
Voir toutes les images disponibles avec la commande : docker images
docker run -d -p 80:80 -p 3306:3306 8d876406448a
<br/><br/>
Voir tous les conteneurs démarrés et les ids associées avec la commande : docker ps<br/>
Entrer dans le bash de Nginx avec l'id de status du conteneur : docker exec -it 8d876406448a bash<br/>
Mise à jour de l'image Docker Lamp MySQL PHP5 curl : update upgrade
Installation du paquet php5-curl
<br/><br/>
Les fichiers du site par défaut une fois connecté à l'image Docker : /var/www/html# ls<br/>

### Sauvegarde de l'image avec cURL
Commiter le conteneur Docker avec Lamp MySQL PHP5 cURL pour générer l'état à sauvegarder.<br/>
Identifier le conteneur a commiter avec la commande : docker ps -a<br/>
Lancer le commit sur le conteneur avec la commande : docker commit -a "Auteur" -m "message optionnel" <ID du conteneur ou nom> <Tag à donner à l'image>
<br/><br/>
Sauvegarder l'image Docker avec Lamp MySQL PHP5 cURL<br/>
Trouver l'id de l'image a sauvegarder avec la commande : docker images -a<br/>
docker save -o /home/seo/lamp-mysql-php5-curl.tar c1d0dc8367a4
