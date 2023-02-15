 RAPPORT D'ANALYSE D'INCIDENT

Date du rapport: 15/02/2021
Préparé par DJANKOU NDJONWOU simplice Edgard 
Incident: compromission du site web
Conséquence: intérruption et isolement du serveur web
Type d'incident: 

       RESUME DE L'INCIDENT

suite a l'attaque que le site bosch-cyber a subit, il en ressort que 
l’attaquant aurait exfiltré des outils secrets très dangereux; 
cependant, le site a été mis en maintenance, afin de découvrir ce que l’attaquant a 
exfiltré

	INTRODUCTION

Bosch-cyber étant une entreprise de la place comme les autres, elle 
s'est vu pirater il y'a de cela peu et son soucis est de savoir la 
méthode utilisé par le hacker pour compromettre son système 
d'information, Dans le but de retracer le parcours utilisé par ce 
dernier, nous allons mettre en place les outils nécessaire et suivre 
les procédures adéquates pour réaliser cet exercice


	METHODOLOGIE


en ce qui concerne la méthode utilié pour mener a bien notre 
investigation, nous avons tout dabord vérifier l'ensemble des logs du 
serveur. en filtrant et en pointant le tout avec les commandes, 
exactement sur les logs qui nous intéresse, on obtient un ensemble 
d'actions qui ont été faites sur le système d'information. Par la 
suite, nous allons vérifier l'activité des utilisateurs ainsi que tous 
les répertoires histoire de vérifier s'il y'a eu une éventuelle 
modification ou un ajout d'un fichier dans le système. Et bien 
évidemment au final nous allons de par ces informations retracer 
l'action ménée par le hackeur.


	RESULTATS

En ce qui concerne les Logs, lorsqu'on se positionne dans 
/var/log/apache2, nous avons accès aux différents logs et lorsqu'on 
affiche le log des érreurs, on se rend compte qu'il y'a les erreus de 
connexion ceci dit qu'il y'a eu plusieurs tentatives de connexions et 
lorsqu'on observe au niveau de "access log" on se rend compte qu'il y'a 
différentes requêtes émises vers le serveur. Par la suite lorsqu'on 
examine les activités éffectués sur le serveur, on se rend compte que 
l'attaquant a:
 -  fait un "cat /etc/passwd" pour voir les utilisateurs qui 
peuvent se connecter au système
 - exécuter un "cat /etc/hosts" afin d'afficher les adresses IP et les 
noms d'hotes assosiés
 - ensuite avec la commande "ls /var/www/html" il a listé le dossier html histoire de confirmer l'existence 
d'un site html
 - il a à partir de l'utilisateur b0sch vérifier le niveau de sécurité 
des comptes utilisateurs et par la suite avec un "crontab", il a crée 
une tâche planifiée
 - il a créer un dossier dans le repertoire Opt ou il a déplacer le 
fichier bosch_cyber_tools.zip
 - A la fin il a supprimé le fichier dézippé bosch_cyber_tools ainsi 
que le fichier "mypassword" das le temp dans le but d'éffacer les 
traces

 
	CONCLUSION

 Après investigations, on se rend compte que le hackeur a tout d'abord 
créer une brèche sur le serveur en envoyant des requêtes et ceci lui a 
permit de s'introduire sur le serveur qui par la suite a pu introduit 
un fichier qui lui permettra grace a la tâche planifiée de s'exécuter 
régulièrement pour lui envoyer des informations

	RECOMMENDATIONS

 Dans le but de prévenir et d'empêcher ce type d'incident, il est 
nécessaire de restraindre voir rendre impossible les injections de 
données sur le serveur web, mettre en place un gestionnaires de logs. 
il est aussi très important de filtrer le traffic entrant et sortant 
sur le serveur et surtout de ne pas laisser les ports pa défaut

	CONCLUSION GENERALE
 Le serveur b0sch-cyber ayant connu une attaque, il était important de 
décéler quelle type d'attaque et reconstituer le scénario de l'attaque. 
Après étude, nous avons constaté que le hackeur avait fait des 
injections sur le serveur ce qui lui a ouvert un accès et par cet accès 
il a pu introduire un fichier compromis qui devait permettre ici grâce 
a la tâche planifiée de l'envoyer des informations de manières 
reccurente. l'analyse étant faite, il est a noter que les mésures de 
sécurité approprié devront être appliquées sur le dit serveur et que 
les logs devront être vérifés de facon réccurentes histoire d'éviter ce 
type d'incident dans les années a venir.
 

Images associées 

/home/jack/Bureau/error log.png
/home/jack/Bureau/historique.png
/home/jack/Bureau/Access log.png
