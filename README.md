# Analyse et Pré-traitement des Données HMMF

Ce projet Python a pour objectif l'analyse, le nettoyage et la correction des données provenant d'un sous-système de filtration HMMF (High-Rate Multi-Media Filter). Les données sont issues de capteurs mesurant les niveaux d'eau, les débits et les pressions différentielles à différents points du système.

---

## 📂 Contenu du projet

Le projet contient les fichiers suivants :

- **Notebooks Jupyter (`.ipynb`)** :
  - `data_cleaned_indexed.ipynb` : Chargement et exploration des données nettoyées.
  - `data_drop_duplicates.ipynb` : Suppression des doublons et premières visualisations.
  - `describe_dataset.ipynb` : Résumé statistique complet du dataset.
- **Fichiers CSV** (ignorés dans Git, mais utilisés pour le traitement) :
  - `data.csv`, `data_drop_duplicates.csv`, `data_final_cleaned_indexed.csv`, `pre_data.csv`
- **Ressources** :
  - Dossier `resources/` contenant éventuellement des fichiers de configuration ou images pour le projet.

---

## 📝 Objectifs

1. **Exploration et visualisation des données** :
   - Comprendre la distribution des variables mesurées par les capteurs.
   - Identifier les anomalies, valeurs manquantes ou aberrantes.

2. **Pré-traitement et nettoyage** :
   - Sélectionner uniquement les colonnes pertinentes pour l’analyse.
   - Corriger les valeurs incohérentes, notamment les niveaux d’eau ou débits à 0 qui ne correspondent pas à un arrêt réel.
   - Détecter et corriger les runs courts de zéros pour éviter les erreurs dues aux capteurs.

3. **Analyse des séquences et des anomalies** :
   - Identifier les séquences où le débit est nul mais la pression différentielle est positive.
   - Appliquer des corrections basées sur le contexte (valeurs avant et après la séquence).

4. **Visualisation** :
   - Comparaison graphique avant/après correction.
   - Analyse temporelle des débits (FIT) et pressions différentielles (PDIT) pour chaque filtre HMMF.

---

## ⚙️ Technologies et bibliothèques utilisées

- Python 3.x
- Jupyter Notebook
- Pandas, NumPy pour la manipulation des données
- Matplotlib, Seaborn pour la visualisation
