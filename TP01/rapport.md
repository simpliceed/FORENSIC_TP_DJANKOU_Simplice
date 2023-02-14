Introduction
 
 L'analyse forensique nécessite de respecter les bonnes pratiques en utilisant les outils adéquates pour analyser, comprendre les évènements passés et en extraire des conclusions. Il est nécessaire de la mettre en place lors d'une attaque informatique ou d'un incident informatique histoire de rejouer les étapes utilisées pour mettre en place la menace. Dans ce cas il sera question de trouver des éléments essentiels inclus dans la clé et pouvant résoudre le mystère.
  
  Etat de l'Art
  
  Pour parvenir à résoudre ce problème, nous commençons par identifier le contexte afin de récupérer les informations et il en ressort que l'objet de notre étude est une clé ramassée à proximité du poste de police contenant des informations protégées.
  L’attaque dans ce cas de figure n'est pas directe mais consiste à utiliser de la malice tout en se reposant sur la curiosité humaine. En effet, l'attaquant espère que une fois la clé ramassée, elle puisse être introduit sur une machine du commissariat et après cela ce dernier devra trouver une porte d'entrée au sein du système d'information du commissariat et procéder à l'attaque proprement dite.
  Une fois la clé en notre possession, nous allons mettre en place le laboratoire nous permettant de réaliser notre investigation. Nous avons procédé à l'installation de UBUNTU en Machine virtuelle, et par la suite nous avons accéder au contenu de la clé que nous avons dézippé et on a découvert des données inaccessibles. Néanmoins nous n'en sommes pas rester là, nous avons par la suite utiliser la commande "foremost" pour récupérer tout simplement les fichiers qui ont été effacés histoire de reconstruire l'index de la partition effacée, ensuit une fois entrer dans un des fichiers effacés, nous avons pu trouver les fichiers dont on avait besoin et nous avons exécuter un "eog" pour afficher les différentes images qui y apparaissaient. Sur une de ces images y'avait notre indice qui permettait de resourdre le problème. 
  
  Conclusion
  
A la suite de cet investigation, nous allons procéder à un reporting auprès des personnes concernés et nous allons souligner que tout matériel issu de l'extérieur ne doit en aucun cas être branché sur un équipement du commissariat et encore seul les équipements ou périphériques fournis par la cellule informatique doivent être connecté aux système d'information du commissariat
https://github.com/simpliceed/FORENSIC_TP_Simplice_DJANKOU/blob/main/TP01/Capture%20d%E2%80%99%C3%A9cran%202023-02-13%20220004.png

