# Étude de Faisabilité et Classification Automatique d'Articles

## Contexte du Projet

"Place de marché" est une entreprise lancée dans la création d'une marketplace e-commerce anglophone. Cette plateforme permet aux vendeurs de proposer des produits à des acheteurs via des photos et des descriptions. À ce jour, l'attribution manuelle des catégories par les vendeurs est peu fiable et ne peut pas suivre l’augmentation du volume des articles. Dans le but d'automatiser cette tâche et améliorer l'expérience utilisateur, "Place de marché" sollicite un Data Scientist pour étudier la faisabilité d'un moteur de classification automatique, utilisant à la fois les images des produits et leurs descriptions textuelles.

Après cette étude de faisabilité, le projet se poursuit avec la mise en place d'un modèle de classification supervisée pour affiner et optimiser la classification des produits, en particulier pour une nouvelle gamme de produits d'épicerie fine. Cela inclut également la collecte et le traitement de données à partir d'API externes et la création d'un notebook Python pour automatiser l'extraction d'informations pertinentes.
Objectifs du Projet

Les objectifs principaux de ce projet sont :

1. Étude de faisabilité d'un moteur de classification d'articles :
- Analyser les descriptions textuelles et les images des produits pour tester la possibilité de regrouper des articles en catégories automatiquement.
- Réaliser une étude visuelle et calculer des mesures de similarité entre catégories réelles et catégories issues d'une segmentation par clustering.

2. Implémentation d’une classification supervisée d’images :
- Appliquer une classification supervisée en utilisant des images de produits.
- Implémenter une technique de data augmentation pour améliorer la performance du modèle.
- Élargir le champ d’application aux produits d’épicerie fine, en utilisant des API externes pour collecter des données spécifiques (par exemple, des produits à base de "champagne").
- Créer un script Python pour l'extraction de données produits en format CSV.

## Données

Les données fournies pour ce projet incluent des informations sur des produits disponibles sur la marketplace de "Place de marché", avec pour chaque produit :
- Image : photo du produit.
- Description textuelle : texte qui décrit le produit.
- Catégorie réelle : catégorie dans laquelle l'article est classé (manuellement par les vendeurs).

Une fois les résultats de l’étude de faisabilité établis, de nouvelles données sont collectées via des API externes (par exemple, Open Food Facts) pour tester l’élargissement de la classification aux produits d’épicerie fine.

## Méthodologie

1. Étude de faisabilité du moteur de classification
- Prétraitement des données : Nettoyage et transformation des descriptions textuelles et des images.
- Extraction de features pour les textes : Utilisation de méthodes comme le bag-of-words (comptage de mots, Tf-idf), ainsi que des word embeddings avec des techniques telles que Word2Vec, BERT et USE.
- Extraction des features pour les image : Utilisation d'algorithmes comme SIFT/ORB/SURF, ainsi que des modèles CNN pour l’extraction de features via Transfer Learning.
- Réduction de dimension : Projection des produits sur un graphique 2D, où chaque point représente un produit et sa couleur correspond à sa catégorie réelle.
- Analyse du graphique : Visualisation des produits et évaluation de la faisabilité de la classification automatique des articles en fonction de leur texte et image.
- Mesure de similarité : Évaluation de la précision du clustering et de la classification avec des mesures de similarité entre les catégories réelles et les catégories issues du modèle de clustering.

2. Classification supervisée d’images
- Data Augmentation : Application de techniques pour augmenter la diversité des données d’entraînement et améliorer la robustesse du modèle de classification.
- Entraînement d’un modèle supervisé : Utilisation d’un modèle préexistant ou création d’un modèle adapté aux images de produits pour prédire les catégories.
- Test et validation : Validation du modèle à l’aide de jeux de données étiquetés et évaluation de sa performance sur de nouvelles images.
- Collecte de données produits d’épicerie fine : Utilisation de l’API Open Food Facts pour récupérer des produits à base de “champagne” et extraction des 10 premiers produits sous format CSV avec diverses informations.

3. Synthèse et Rapport
- Préparation d’un rapport final : Résumé de l’analyse, des méthodes employées, des résultats obtenus et des conclusions sur la faisabilité du projet.
- Présentation des résultats : Rédaction d’une présentation au format PDF de 30 slides maximum, détaillant la démarche et les résultats clés du projet.

## Outils et Technologies

Pour la réalisation du projet, les outils suivants seront utilisés :
- Bibliothèques : Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn pour l’analyse et la visualisation.
- Traitement d’images : OpenCV pour les algorithmes SIFT/ORB/SURF et TensorFlow ou Keras pour l’utilisation de CNN et Transfer Learning.
- Traitement de texte : NLTK, spaCy, Gensim, Transformers pour l'extraction des features textuelles (Word2Vec, BERT, etc.).
- API : Requests pour l'interaction avec les API externes comme Open Food Facts.

## Résultats et Application

Le projet permettra à "Place de marché" de mettre en place une solution automatique et efficace pour classifier les produits dans des catégories adaptées, à la fois en fonction de leur description et de leur image. Cette approche pourra être élargie à des produits spécifiques comme ceux de l’épicerie fine, et améliorée au fil du temps grâce à l’utilisation de techniques avancées comme le Transfer Learning et la data augmentation.

Les résultats obtenus seront partagés sous forme d’un rapport détaillant la méthodologie et les conclusions, ainsi qu'une présentation synthétisant les principales découvertes et recommandations pour les prochaines étapes du projet.
