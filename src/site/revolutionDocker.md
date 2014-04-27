La révolution Docker

La conférence a été présentée par Nicolas De Loof de chez Cloud Bees et de Champiii. De chez Google.

C était tout seul sur l’estrade à pprésenté le sujet. Et d’un coup on entend un mégaphone venant du fond de la salle. C’était Nicolas qui était déguisé en docker et tenait à la main un drapeau blanc.


Docker est un «conteneur, isolateur qui permet de virtualiser un système d’exploitation.

Sa grande différence avec Virtual Box & Cie, c’est qu’il ne virtualise que le noyau des systèmes d’exploitations basés sur Linux. De plus, pour l’instant il ne fonctionne que sur ces systèmes. Il n’est pas encore disponible sur Windows.
Cependant, il fonctionne sur Mac OS après quelques paramétrages.

Il se base sur LMCTFY de chez Google.

Voici les points forts :
•	Construction incrémentale des images via le dockerfile
•	On exécute les commandes de l’hôte vers l’image docker
•	Les deux environnements sont confondus visuellement mais au fait ils ne le sont pas. La machine virtuelle est bien séparée. Une des questions posée portait justement sur cette confusion.
•	Intérêts :
o	Portabilité et reproduction des environnements de dev et de prod plus facilement.
•	Il a montré l’intégration avec Jenkins.
o	Construction de l’image pour les tests d’intégration
•	Intégration dans Google Cloud Plateforme (mettre lien vers l’article)
o	Existence d’un outil boot2docker pour mac utilise virtual box
o	Existence d’un registre privé si on ne veut pas partager son image avec le reste du monde. Bien sûr cette solution est payante.
•	Posibilité de partager et de récupérer des images d’autres personnes depuis l’Index Docker qui regroupe les images partagées.
•	Il n’est pas nécessaire de connaître la configuration de la plateforme de PROD par exemple, le chemin où sera déployé l’application.
•	Modularité : micro-services & communication
•	Java the « unix-way »
•	Docker ps run


