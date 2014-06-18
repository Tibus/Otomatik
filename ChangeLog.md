ChangeLog
=========
**V0.0.8 (futur)**:
 - Ajout d'un systeme de reconnaissance vocal interne avant la reconnaissance vocale de Sarah (si on a un serveur Sarah) pour permettre d'allumer, éteindre, ouvrir, fermer, faire varier,... n'importe quel portlet de l'application.
 - Ajout d'un écran "Liste" qui affiche tous les devices sous forme de liste que l'on peu classer par nom, type ou écran de la page d'accueil. En slidant horizontalement chaques items, on peut faire apparaître une bouton supprimer, editer et afficher sur la page d'accueil. La pluspart des items garde leurs fonctionnalité d'intéraction (bouton on/off, dimmer, affichage des valeurs d'un sensor,...)
 - Ajout d'une fonctionnalité pour masquer un portlet de la page d'accueil (mais il reste afficher dans la page "liste") (pas encore pour tous les portlets car ils ne se retrouvent pas encore tous dans la page "liste")
 - Possibilité de gérer la sécurité d'accès à un serveur indépendament en local et en externe
 - Correction des connexions SSL et Basic Auth
 - Meilleur gestion de la connexion aux serveurs
 - Nouveau manager de reconnaissance vocale (pour permettre la reconnaissance vocale)
 - Ajout d'un portlet de texte simple sans background
 - Possibilité de mettre à jour un sensors en cliquant sur le portlet
 - Intégration de la reconnaissance vocale directement dans le portlet de reconnaissance vocale
 - Ajout/suppression des écrans en fonction des serveurs ajouté (ne pas afficher les écrans propre à S.A.R.A.H. s'il n'y a pas de server configuré par exemple)
 - changement des requètes de récupération des valeurs de sensors de Domoticz (ça fait beaucoup de "De") pour permettre :
 - Regroupement des requètes de récupération des sensors et autres pour diminuer le nombres de requêtes sortantes. (Plus particulièrement pour les box domotiques qui, en une requête, peuvent récupérer l'état de tous les sensors)
 - Ajout de la date sur le portlet d'horloge

***interne***
 - refacto du systeme de connexion et de Sécurité.
 - refacto complète du systeme de portlet et de leurs actions pour la centralisation de tous les portlets
 
**V0.0.7.1 (4 juin 2014)**:
 - bug fix à l'ajout automatique des sensors domoticz
 
**V0.0.7 (4 juin 2014)**:
 - nouveau nom : Otomatik
 - qui dis nouveau nom, dis nouveau logo
 - Correction d'un bug lié à la reconnaissance vocale et l'envoi à Sarah (qui retournai toujours une erreur de connexion)
 - Possibilité d'utilisé domoticz sans login/mdp ainsi que de passer par de l'HTTPS, login/mdp d'une autre méthode que Domoticz,...
 - correction d'un bug lié au "off" d'un dimmer sur domoticz
 - nouveau systeme de connexion et de vérification de la connexion de chaque serveur
 - correction graphique et bug fix sur la création d'action lié à domoticz.

**V0.0.6 (3 juin 2014)**:
 - ajout d'un widget de récupération de données (température, vent, pourcentage,...)
 - intégration du serveur domoticz et de la pluspart de ses fonctionnalités (possibilités de créer des boutons automatiquement initialisé, d'utiliser domoticz dans des actions personnalisées et possibilités de remplir la home automatiquement avec les devices domoticz)
 - ajout d'un widget avec l'heure
 - reduction de la taille minimal des portlets et possibilité de définir la taille de la pluspart des portlets
 - nouveau design pour le portlet de Variateur
 - début d'homogénéisation des couleurs et agrandissement des contenus de modalBox,...
 - Correction de plusieurs bugs
 - remplacement des radioButton par des listes beaucoup plus pratique.
 - ajout d'une nouvelle clé pour google speech V2;
 
**V0.0.5 (12 mai 2014)**:
  - permettre d'ajouter plusieurs serveur/box domotique/serveur Sarah en même temps. on utilise alors le raccourcis (définis par l'utilisateur) d'un serveur dans l'url (par exemple "$$raspberrypi") et l'application s'occupe de gerer l'url (local ou global), la sécurité, login/mots de passe, header SSL,...
  	 (pour l'instant uniquement une configuration par Défaut autre que Sarah qui permet de lancer des requetes sur une url local/global pour controler un PC, une box domotique en http,...). Il reste encore à activé/désactivé les screens de l'application en fonction des serveur présent (ne pas afficher l'écran de reconnaissance vocale si aucuns serveur sarah n'est configuré par exemple)
  - intégration de google speech V2 à la version IOS/PC/MAC, la version Android n'étant pas touchée...
  - Ajout d'une fonctionnalité dans chaques actions permettant de n'envoyer l'action que sur l'url local d'un serveur. (même si l'url global du serveur est accessible et pas l'url local, la requète sera quand même testée sur l'url local) (pour, par exemple ne pouvoir allumé une lampe que si on est connecté au wifi de sa maison)
  - Ajout d'un mode Debug pour afficher l'erreur d'une requète envoyé depuis la home. (les autres screen affiche tout le temps une modal box d'erreur mais la home ne l'affiche que quand on est en mode debug) (va de paire avec la fonctionnalité de requète uniquement en local. comme ça, si on est pas en local, il test la requète local qui ne marchera pas et n'affichera pas d'erreur.)
  - portlet XBMC connecté en socket qui récupère les events, se mets à jours automatiquement en direct (même si XBMC est contrôlé avec une autre télécommande), si XBMC à besoin d'un clavier, un clavier s'affiche dans le portlet et est connecté au clavier de XBMC et, aussi, la présence d'une télécommande pour controler le player, l'UI,...
  - Ajout de la gestion de suppression des icônes photos dans la page de config
  - Correction du bug : "Quand on vocalise quelque chose et que sarah retourne un tts vide, l'application dis qu'elle n'a pas compris ou que c'est la même réponse alors que c'est juste vide..."
  - attendre quelques secondes pour l'affichage d'erreur de connexion à l'ouverture de l'application pour pas afficher l'erreur s'il n'y en a pas
  - ajout d'un systeme de cache pour les XML de langue de Sarah. On peut donc créer des phrases même si le server sarah n'est pas accessible. on les recharge dés qu'on a une connexion au server pour les mettre à jour...
  - ajout d'une meilleur gestion d'édition de texte pour tous les textes
  - Gestion de l'orientation des photos quand on ajoute une icône (lecture des données EXIF de la photo avant de l'orienter)
  - ajout de login/mots de passe pour l'accès WEB/local (soit en clair dans l'url, soit chiffré dans le header avec la méthode de base)
  - ajout du https pour les requètes
  - ajout de la possibilitées de changer chaques titres de chaque screen de l'acceuil.
  - réorganisation des fichiers et du repo HG pour pouvoir balancer plus souvent et plus facilement des correctifs mineurs,...
  - amélioration du systeme de grille de la page d'acceuil
  
**V0.0.4 (23 mars 2014)** :
  - ajout de la possibilités de choisir parmis les photos existantes ou de prendre une nouvelle photo pour s'en servir comme icône.
  - ajout de la sauvegarde de la configuration de l'application (icone/ip/ports/favorits/acceuil/requète,...) sur Dropbox (en attente d'approbation par dropbox) et/ou sur Google Drive.
  
**V0.0.3 (20 mars 2014)** :
  - correction de quelques bugs d'orientation et de fullscreen
  - ajout du numéro de version en arrière plan
 
**V0.0.2 (19 mars 2014)** :
  - ajout du choix d'orientation (portrait ou paysage)
  - ajout d'un widget pour la reconnaissance vocale
