ChangeLog
=========

**V0.0.7 (futur)**:
 - nouveau nom : Otomatik
 - qui dis nouveau nom, dis nouveau logo
 - Correction d'un bug lié à la reconnaissance vocale et l'envoi à Sarah (qui retournai toujours une erreur de connexion)
 - Possibilité d'utilisé domoticz sans login/mdp ainsi que de passer par de l'HTTPS, login/mdp d'une autre méthode que Domoticz,...
 - correction d'un bug lié au "off" d'un dimmer sur domoticz
 - 
 - nouveau systeme de connexion et de vérification de la connexion de chaque serveur

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
