Introduction
 
 L'analyse forensique nécessite de respecter les bonnes pratiques en utilisant les outils adéquates pour analyser, comprendre les évènements passés et en extraire des conclusions. Il est nécessaire de la mettre en place lors d'une attaque informatique ou d'un incident informatique histoire de rejouer les étapes utilisées pour mettre en place la menace. Dans ce cas il sera question de trouver des éléments éssentiels inclus dans la clé et puvant résoudre le mystère.
  
  Etat de l'Art
  
  Pour parvenir a resourdre ce problème, nous commencons par identifier le contexte afin de récupérer les informations et ils en ressort que l'objet de notre étude est une clé ramassé a proximité du poste de police contenant des informations protégées.
  l'attaque dans ce cas de figure n'est pas directe mais consiste a utiliser de la malice tout en se reposant sur la curiosité humaine. en éffet, l'attaquant espère que une fois la clé ramassé, elle puisse être intoduit sur une machine du commissariat et après cela ce dernier devra trouver une porte d'entrée au sein du système d'information du commissariat et procéder a l'attaque proprement dite.
  une fois la clé en notre possession, nous allons mettre en place le laboratoire nous permettant de réaliser notre investigation. Nous avons procéder a l'installation de UBUNTU en Machine virtuelle, et par la suite nous avons accéder au contenu de la clé que nous avons dézippé et on a découvert des données innacéssible. Neammoins nous n'en sommes pas rester là, nous avons par la suite utiliser la commande "foremost" pour récupérer tout simplement les fichiers qui ont été éffacés histoire ed reconstruire l'index de la partition éffacée, ensuit une fois entré dans un des fichiers éffacés, nous avons pu trouver les fichiers dont on avait besoin et nous avons exécuter un "eog" pour afficher les différentes images qui y apparaissaient. sur une de ces images y'avait notre indice qui permettait de resourdre le problème. 
  
  Conclusion
A la suite de cet investigation, nous allons procéder a un reporting auprès des personnes concernés et nous allons souligner que tout matériel issu de l'extérieur ne doit en aucun cas être branché sur un équipement du commissariat et encore seul les équipements ou périphériques fournis par la cellule informatique doivent être connecté aux système d'information du commissariat
