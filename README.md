# **Challenge DataTour 2024 - Phase Nationale: Prévision de la Production d’Énergie Solaire en Afrique**

## **Contexte**

L'accès à une énergie fiable reste un défi majeur en Afrique subsaharienne. Pour améliorer l’allocation des ressources énergétiques et développer les infrastructures solaires, il est crucial de prédire la demande énergétique dans différentes régions. Ce projet s’inscrit dans le cadre de la compétition **DataTour 2024**, où l’objectif est de construire un modèle de régression performant pour estimer la demande énergétique projetée en Afrique, en tenant compte des facteurs géographiques, socio-économiques et environnementaux.

## **Objectif**

Le but de cette compétition est de développer un modèle de régression afin de prédire la **demande énergétique projetée** pour des régions spécifiques, en utilisant un ensemble de caractéristiques telles que la localisation, la population, la capacité énergétique installée, le taux d'ensoleillement et d'autres facteurs clés.

## **Structure des Données**

Les données sont divisées en trois fichiers principaux, chacun ayant un rôle spécifique dans l'entraînement et l'évaluation du modèle :

1. **train.csv**
   - **Taille** : 150 000 lignes.
   - **Colonnes** : Inclut toutes les variables, y compris la cible `demande_energetique_projectee`.
   - **Utilisation** : Utilisé pour entraîner le modèle.

2. **test.csv**
   - **Taille** : 62 500 lignes.
   - **Colonnes** : Contient toutes les variables nécessaires à l'ajustement du modèle.
   - **Utilisation** : Ce fichier est utilisé pour valider la performance du modèle avant la soumission.

3. **submission.csv**
   - **Taille** : 25 000 lignes.
   - **Colonnes** : Contient toutes les caractéristiques sauf la cible `demande_energetique_projectee`.
   - **Utilisation** : Fichier de soumission où les prédictions doivent être générées.

## **Description des Colonnes**

Les colonnes des fichiers contiennent des informations géographiques, socio-économiques et environnementales sur chaque région, permettant de mieux comprendre les besoins énergétiques.

| Colonne                              | Description                                                                                                    |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------|
| `country`                            | Pays de la région.                                                                                             |
| `lat`, `lon`                         | Latitude et longitude.                                                                                        |
| `population`                         | Population de la région.                                                                                       |
| `taux_ensoleillement`                | Moyenne du taux d’ensoleillement annuel.                                                                        |
| `demande_energetique_actuelle`       | Demande énergétique actuelle de la région.                                                                      |
| `demande_energetique_projectee`      | La cible à prédire, la demande énergétique projetée.                                                            |
| `capacite_installee_actuelle`        | Capacité énergétique installée dans la région.                                                                 |
| `duree_ensoleillement_annuel`        | Nombre moyen d'heures d’ensoleillement annuel.                                                                  |
| `cout_installation_solaire`          | Coût pour installer des infrastructures solaires dans la région.                                                |
| `proximite_infrastructures_energetiques` | Distance aux infrastructures énergétiques existantes.                                                      |
| `taux_adoption_energies_renouvelables` | Pourcentage de la population utilisant des énergies renouvelables.                                           |
| `stabilite_politique`                | Score de stabilité politique.                                                                                  |
| `taux_acces_energie`                 | Pourcentage d’accès à l’énergie dans la région.                                                                |
| `niveau_urbanisation`                | Niveau d’urbanisation.                                                                                         |
| `potentiel_investissement`           | Indicateur du potentiel d'investissement dans la région.                                                        |
| `types_sols`                         | Types de sols.                                                                                                 |
| `emissions_co2_evitees`              | Estimation des émissions de CO₂ évitées grâce aux énergies renouvelables.                                      |
| `idh`                                | Indice de développement humain.                                                                                |

## **Métrique d’Évaluation**

La performance du modèle sera mesurée par la **Root Mean Squared Error (RMSE)**. La formule est la suivante :

$$
RMSE = \sqrt{\frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2}
$$

- $y_i$ : Valeur réelle de la demande énergétique projetée.
- $\hat{y}_i$ : Prédiction du modèle.
- $n$ : Nombre total d’observations.

Le modèle avec le plus bas RMSE sera classé en tête.

## **Tâches du Projet**

1. **Exploration des données** : Analyser les relations entre les caractéristiques et identifier les plus influentes pour prédire la demande énergétique.
2. **Modélisation** : Développer un modèle de régression (par exemple, Random Forest, Gradient Boosting, ou Réseaux de Neurones) pour prédire la demande énergétique projetée.
3. **Optimisation** : Affiner les hyperparamètres et éviter le surajustement en utilisant des techniques de validation croisée.
4. **Prédictions** : Générer les prédictions sur le fichier `submission.csv` et les soumettre dans le format spécifié.

## **Critères de Soumission**

Les fichiers de soumission doivent être au format CSV, comprenant les colonnes suivantes :
- `id` : Identifiant de chaque ligne.
- `demande_energetique_projectee` : Prédiction de la demande énergétique projetée pour chaque région.

Exemple de format :
```csv
id,demande_energetique_projectee
1,12345.67
2,8910.11
3,34567.89
...
```

## **Contribuer au Projet**

Les contributions à ce projet sont les bienvenues. Pour commencer :
1. Fork ce repository.
2. Crée une branche pour tes modifications (`git checkout -b feature-xyz`).
3. Fais un commit de tes modifications (`git commit -am 'Add new feature'`).
4. Push vers la branche distante (`git push origin feature-xyz`).
5. Ouvre une Pull Request.

## **Auteurs**

- **Wendyellé Abubakrh Alban NYANTUDRE**  
  - ✉️ Email : nyantudrealban@gmail.com
  - 🌐 LinkedIn : [linkedin.com/in/anyantudre](https://www.linkedin.com/in/anyantudre/)
  
- **Haitam Bouanane**  
  - ✉️ Email : bouananehaitam03@gmail.com
  - 🌐 LinkedIn : [linkedin.com/in/haitam-bouanane-656783221](https://ma.linkedin.com/in/haitam-bouanane-656783221)
  
- **Hatim Belfarhounia**  
  - ✉️ Email : nothatim@gmail.com
  - 🌐 LinkedIn : [linkedin.com/in/hatim-belfarhounia-7a8932291](https://www.linkedin.com/in/hatim-belfarhounia-7a8932291)

Nous remercions chaleureusement **Data Afrique Hub** pour avoir fourni les datasets et organisé cette compétition exceptionnelle.