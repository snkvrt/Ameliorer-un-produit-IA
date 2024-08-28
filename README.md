# Vous êtes Ingénieur IA au sein de la startup “Avis Restau”, qui met en relation des clients et des restaurants.


Votre entreprise souhaite améliorer sa plateforme avec une nouvelle fonctionnalité de collaboration. Les utilisateurs pourront par exemple poster des avis et des photos sur leur restaurant préféré. Ce sera aussi l’occasion, pour l’entreprise, de mieux comprendre les avis postés par les utilisateurs.

Ider, le CTO de l’entreprise, vous a transmis le cahier des charges simplifié suivant :

 
Use Case

En tant qu’utilisateur de Avis Restau, je peux :

poster des avis sous forme de commentaires.
poster des photos prises dans le restaurant.

En tant qu’Avis Restau, je souhaite :

Détecter les sujets d’insatisfaction présents dans les commentaires postés sur la plateforme.
Labelliser automatiquement les photos postées sur la plateforme. Par exemple, identifier les photos relatives à la nourriture, au décor dans le restaurant ou à l’extérieur du restaurant.
Scope du projet

Étude préliminaire fonctionnalité “Détecter les sujets d’insatisfaction” et  “Labelliser automatiquement les photos postées”

Jeu de données

Problème : Pas assez de données sur la plateforme Avis Restau.
Solution : utiliser un jeu de données existant.
Lien vers le jeu de données : https://www.yelp.com/dataset
Contient des informations générales (par exemple type de cuisine) et les avis des consommateurs sur les différents restaurants.
Au vu du volume du jeu de données, pour pouvoir le charger entièrement, s’aider de cet article.
Collecte des données

Problème : s’assurer de la possibilité de collecter de nouvelles données.
Solution : collecter de nouvelles données via l’API Yelp. Valider la faisabilité de la solution en collectant les  informations relatives à environ 200 restaurants pour une ville en utilisant l’API.
Lien vers la documentation de l’API Yelp.
Outils

Python et librairies spécialisées NLP/CV.
Jupyter Notebook et package Voilà
Après avoir reçu et étudié ce cahier des charges, vous avez envoyé le mail suivant à Ider :

 

De : Vous 

Envoyé : hier 17:14

À : Ider

Objet : Re: Cahier des charges

Bonjour Ider,

J’ai bien reçu et pris en compte ce cahier des charges. Je t’en remercie.

Voici les différentes étapes que je vais réaliser :

analyser les commentaires négatifs pour détecter les différents sujets d’insatisfaction :
sélection de quelques milliers de commentaires négatifs,
prétraitement des données textuelles,
utilisation de techniques de réduction de dimension,
visualisation des données de grandes dimensions afin de détecter des mots clés et sujets d’insatisfaction ;
analyser les photos pour déterminer les catégories des photos : 
sélection de 100 à 200 photos par catégorie,
prétraitement des images. Je vais tester deux approches, une par extraction de descripteurs (SIFT, ORB ou SURF) et une par Transfer Learning d’un réseau de neurones de type CNN,
utilisation de techniques de réduction de dimension,
visualisation des données de grandes dimensions en mettant en évidence les catégories des images,
vérification que les images sont correctement regroupées selon les catégories en réalisant un clustering, puis une comparaison des clusters avec les catégories des images, via un graphique et une mesure. Je vais analyser également quelles sont les catégories les mieux regroupées,
cette vérification me permettra de conclure sur la faisabilité de réaliser ultérieurement une classification supervisée, j’ai bien compris qu’il n’était pas nécessaire à ce stade de réaliser cette classification supervisée ;
collecter un échantillon de données (environ 200 restaurants et leurs revues) via l’API Yelp :
récupérer uniquement les champs nécessaires,
stocker les résultats dans un fichier exploitable (par exemple CSV).
Je te présenterai mon travail en illustrant au maximum pour le rendre facilement compréhensible lors de notre prochain point.

A bientôt.


Et Ider vous a renvoyé ce mail :

 
Hello !

Merci pour ton mail de récap : nous sommes tout à fait alignés !

Bon courage pour le démarrage, et j’attends avec impatience ta présentation.

A bientôt,

Ider

Attention, Ider n’a pas besoin à ce stade d’un moteur de classification supervisée, ni pour le texte, ni pour les images, mais bien d’une étude de faisabilité!

Livrables  
Un fichier csv contenant les informations sur les restaurants collectées en utilisant l’API Yelp :
Ce livrable vous servira à montrer la possibilité de collecter de nouvelles données directement via l’API
Un Jupyter Notebook présentant les différentes parties de votre travail de collecte, de pré-traitement des données textes et images et des réductions de dimension associées  ;
Ce livrable devra être autoporteur.
Une page web avec des représentations graphiques des données textes et images (via le package Voilà ! par exemple) :
Ce livrable vous servira à synthétiser les résultats de votre analyse lors de la présentation à Ider, le CTO
Un support pour la présentation orale du travail.
Pour faciliter votre passage devant le jury, déposez sur la plateforme, dans un dossier zip nommé “Titre_du_projet_nom_prénom”, votre livrable nommé comme suit : Nom_Prénom_n° du livrable_nom du livrable_date de démarrage du projet. Cela donnera : 

Nom_Prénom_1_csv_mmaaaa
Nom_Prénom_2_notebook_mmaaaa
Nom_Prénom_3_page_web_mmaaaa
Nom_Prénom_4_presentation_mmaaaa
Par exemple, votre premier livrable peut être nommé comme suit : Dupont_Jean_1_csv_012022.

Soutenance
La soutenance se déroulera en visioconférence et durera 30 minutes. Votre mentor jouera le rôle d’Ider.

Présentation (20 minutes) 
Visualisations de graphiques (à l’aide d’une page web générée grâce au package Voilà).
Conclusion sur la faisabilité de détection des sujets d’insatisfaction présents dans les commentaires et la labellisation automatique des photos.
Compréhension de la problématique métier et description des jeux de données (2 min).
Détection des sujets d’insatisfaction (5 min).
Labellisation automatique des photos (8 min).
Synthèse (5 min) :
Discussion (5 minutes)
L’évaluateur, jouant le rôle de Ider, vous challengera sur vos choix.
Débriefing (5 minutes)
À la fin de la soutenance, l'évaluateur arrêtera de jouer le rôle d’Ider pour vous permettre de débriefer ensemble.
Votre présentation devrait durer 20 minutes (+/- 5 minutes).  Puisque le respect des durées des présentations est important en milieu professionnel, les présentations en dessous de 15 minutes ou au-dessus de 25 minutes peuvent être refusées. 

Référentiel d'évaluation
Compétences

Critères d'évaluation

Collecter des données venant d’une API qui correspondent à un besoin défini

La collecte des données via une API est complète si :

❒ une requête pour obtenir les données via l’API a été écrite, testée, et renvoie bien des données en retour


La collecte des données via une API est pertinente si :

❒ seuls les champs nécessaires ont été récupérés 

❒ au moins un filtre a été appliqué sur un des champs nécessaires pour ne collecter que les avis ayant les valeurs correspondantes sur ces champs 


La collecte des données via une API est présentable si :

❒ les données collectées via l’API sont stockées dans un fichier utilisable (ex. : fichier CSV, avec en colonnes les différentes informations correspondant aux avis)

Effectuer un prétraitement de données non structurées pour obtenir un jeu de données utilisable

Le prétraitement de données non structurées pour obtenir un jeu de données utilisable est complet si :

❒ les champs de texte sont nettoyés : la ponctuation et les mots de liaison ont été retirés, les chaînes de caractères ont été mises en minuscules

❒ au moins une parmi les trois transformations “stemming”, “tokenization”, “lemmatization” a été appliquée 

❒ le bruit sur les images a été filtré

❒ l’histogramme a été égalisé sur les images


Le prétraitement de données non structurées pour obtenir un jeu de données utilisable est pertinent si :

❒ pour le texte, au moins un bag-of-words a été créé, incluant des étapes de nettoyage supplémentaires, comme un seuil de fréquence et la normalisation des mots 

❒ pour les images, un algorithme d’extraction de features a été créé (ORB, SIFT, SURF), et un algorithme de Transfert Learning basé sur des réseaux de neurones, comme par exemple CNN, a été créé


Le prétraitement de données non structurées pour obtenir un jeu de données utilisable est présentable si :

❒ l’enchaînement des étapes de nettoyage et de création de variables pour les images et le texte a été automatisé (en écrivant les différentes étapes sous forme de fonction, puis en utilisant un pipeline) et a été testé sur un exemple

Utiliser des techniques de réduction de la dimension

L’utilisation des techniques de réduction de la dimension est complète si :

❒ une méthode de réduction de dimension a été appliquée sur les données texte et sur les données images

L’utilisation des techniques de réduction de la dimension est pertinente si :

❒ une justification du fait d’appliquer une réduction de dimension sur les données texte et image a été donnée

❒ une justification des choix des valeurs des paramètres dans la méthode de réduction de dimension retenue a été donnée (ex. : le nombre de dimensions conservées pour l'ACP)

Visualiser des données de grandes dimensions

La visualisation des données en grande dimension est complète si :

❒ au moins un graphique représentant des informations contenant plus de deux dimensions a été réalisé 


La visualisation des données en grande dimension est pertinente si :

❒ le choix de la méthode de représentation graphique a été justifié (T-SNE…)

❒ la lecture du graphique a été facilitée en explicitant les différents éléments pour un public non expert

 

La visualisation des données en grande dimension est présentable si :

❒ le graphique réalisé est lisible et compréhensible (ex. : taille des titres et légende)

 

Compétences évaluées
Collecter des données venant d’une API qui correspondent à un besoin défini
Visualiser des données de grandes dimensions
Effectuer un pré-traitement de données non structurées
Utiliser des techniques de réduction de la dimension
