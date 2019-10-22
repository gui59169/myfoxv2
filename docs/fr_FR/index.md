
 Présentation
===

Plugin permettant de dialoguer avec L'API Myfox api.myfox.me, pour les boxes domotique/alarme Myfox, également valable pour Evology (leroy merlin).


 Prérequis, installation
=== 
Vous devez au préalable récupérer vos identifiants sur http://api.myfox.me (connectez vous avec le m^me identifiant que l'application iphone/android).


Configuration
=== 
Après avoir fait une MISE A JOUR du plugin, vous devez à nouveau sauvegarder l'équipement.


Création et utilisation des équipements  
=== 
Ajoutez un équipement, puis indiquez-y les informations récupérées sur http://api.myfox.me (My applications) :

- Client iD
- Client secret
- Indiquez votre identifiant Myfox
- Indiquez votre mot de passe Myfox

ATTENTION : Ne pas faire d'erreur avec le client id, client secret, id, password. En cas d'erreur, votre compte Myfox sera bloqué pendant 1 heure depuis votre IP.


Fonctionnement du plugin
=== 
Une fois cliqué sur le bouton "sauvegarder" le plugin récupère vos capteurs de température, lumière, actionneur prise, lumière, module, garage... C'est pourquoi il ne faut pas d'erreur dans les identifiants.

Le plugin récupère toutes les minutes :

- L'état de l'alarme (armement total, armement partiel, désarmé)
- La température et luminosité du capteur Myfox TA4007 (si vous en avez un)
	* Luminosité : paliers de retour de 1 à 6 . 1= pleine lumière,  6 = obscurité


- Dernier évènement de type "alarm" ( intrusion, défaut centrale, défaut pile ) sous la forme : "Alarme « Intrusion » déclenchée par l'appareil « ENTREE » (Sensibilité: 5). le xxxx à xxx."
	* S'il n'y a pas d'évènement dans la journée, la commande retourne : Aucun *

Le plugin permet : 

- L'activation (partielle ou totale) et la désactivation de l'alarme
- L'activation ou désactivation d'un équipement (module, prise, lumière, garage, portail)
- L'activation de scénarios enregistrés chez Myfox
