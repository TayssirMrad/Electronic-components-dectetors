# Electronic-components-dectetors : CNN in Edge Impulse
L'objectif de ce projet était d'explorer l'entraînement d'un réseau neuronal convolutif (CNN) à l'aide d'Edge Impulse, en passant au-delà des réseaux neuronaux denses traditionnels. Nous avons utilisé un ensemble de données contenant des composants électroniques, et le projet impliquait la conversion d'images, le téléchargement de l'ensemble de données, la création d'une impulsion, l'extraction de fonctionnalités, et enfin, l'entraînement du CNN.

1. Téléchargement de l'ensemble de données
   
La première étape pour démarrer le projet est d'initier un nouveau projet et de se rendre à la section Acquisition de données. Utilisez la fonction "Télécharger des données existantes" pour intégrer votre ensemble de données de manière transparente. Sélectionnez toutes les images correspondant à une classe spécifique, telle que la classe de résistance, et assurez-vous que l'option "Répartition automatique entre l'entraînement et les tests" est activée. Attribuez un label à votre catégorie, par exemple, "résistance", et lancez le processus de téléchargement en cliquant sur "Commencer le téléchargement". Répétez ce processus pour d'autres catégories. Une fois terminé, inspectez attentivement la représentation des échantillons dans vos ensembles d'entraînement et de test sous l'onglet Acquisition de données pour garantir un ensemble de données équilibré et complet pour un entraînement efficace du modèle.

![P4_dataset](https://github.com/TayssirMrad/Electronic-components-dectetors/assets/60198040/170c387a-e414-4055-9395-35df81ed3577) 


2. Création de l'impulsion
   
La phase de conception de l'impulsion impliquait le paramétrage des dimensions des données d'image, l'ajustement des modes de redimensionnement pour les images non carrées, et l'ajout de blocs nécessaires tels que le traitement d'image et la classification (blocs d'apprentissage Keras). L'impulsion a été enregistrée pour passer aux étapes suivantes.

4. Extraction des fonctionnalités
   
Sous la conception de l'impulsion, les images ont été définies en niveaux de gris, et les fonctionnalités ont été générées. Cette étape impliquait la conversion des images en pixels de 28x28 en niveaux de gris, les préparant ainsi pour la phase d'entraînement du CNN.

![P4_generate_features](https://github.com/TayssirMrad/Electronic-components-dectetors/assets/60198040/938c6f35-546a-48f6-80a8-484a90b42814)


4. Entraînement du modèle
   
Le CNN a été entraîné à l'aide du classificateur NN. Des recommandations ont été fournies pour expérimenter avec les hyperparamètres tels que le nombre de cycles d'entraînement, les filtres et les tailles de noyau. Les utilisateurs ont été encouragés à ajuster l'architecture du modèle, des exemples spécifiques étant fournis. L'importance de l'évaluation de la performance du modèle sur les données de validation a été soulignée.

![P4_training___1](https://github.com/TayssirMrad/Electronic-components-dectetors/assets/60198040/87f1ade6-0a02-4df5-a814-b671d13f5a70)
![P4_training___](https://github.com/TayssirMrad/Electronic-components-dectetors/assets/60198040/22b73e89-3182-41f9-8f5f-495a155d214f)

Après avoir tenté d'ajuster les hyperparamètres du modèle, y compris le nombre de cycles d'entraînement, les filtres et les tailles de noyau, j'ai introduit une couche de désactivation après la première couche de convolution et modifié la deuxième couche de convolution pour incorporer 28 filtres. 

![P4_training___22](https://github.com/TayssirMrad/Electronic-components-dectetors/assets/60198040/2b837c17-6322-42c5-a81c-94df4ec1eb3a)
![P4_training___2](https://github.com/TayssirMrad/Electronic-components-dectetors/assets/60198040/be8b8650-9454-4c8d-aab1-f4a5570b7c84)

5.Conclusion
Grâce à ces ajustements, l'exactitude sur l'ensemble de données de validation a été significativement améliorée. Par exemple, en augmentant le nombre de cycles d'entraînement de 150 à 200 et en introduisant une couche de désactivation après la première couche de convolution, ainsi qu'en modifiant la deuxième couche de convolution pour intégrer 28 filtres, nous avons observé une augmentation de la précision de 90.2% à 95.1%. De plus, une diminution notable de la perte (loss) est également observée, passant de 1.05 à 0.97.
