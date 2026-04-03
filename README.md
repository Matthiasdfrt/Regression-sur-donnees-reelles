<!-- Auteur : Lesueur Romain -->

<div align="center">

<!-- En-tête avec gradient -->
<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=200&section=header&text=Régression%20—%20Indice%20de%20Masse%20Graisseuse&fontSize=36&fontAlignY=35&animation=twinkling&fontColor=fff" />

### **Projet de Statistiques : Modélisation de l'Indice de Masse Graisseuse (FFMI)**

<p align="center">
  <img src="https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white" />
  <img src="https://img.shields.io/badge/ggplot2-2C8EBB?style=for-the-badge&logoColor=white" />
  <img src="https://img.shields.io/badge/Régression_Linéaire-10B981?style=for-the-badge&logoColor=white" />
  <img src="https://img.shields.io/badge/Statistiques-8B5CF6?style=for-the-badge&logoColor=white" />
</p>

<br>

<!-- Badges des technologies -->
<p align="center">
  <img src="https://img.shields.io/badge/Année-2024-F59E0B?style=for-the-badge&logoColor=white" alt="2024" />
  <img src="https://img.shields.io/badge/Langage-R-276DC3?style=for-the-badge&logo=r&logoColor=white" alt="R" />
  <img src="https://img.shields.io/badge/Type-Régression-10B981?style=for-the-badge&logoColor=white" alt="Régression" />
</p>

</div>

<br>

---

## Description du projet

<div align="center">
<table>
<tr>
<td width="70%">

Analyse statistique complète pour déterminer le meilleur modèle de régression linéaire permettant de prédire l'**Indice de Masse Sans Graisse (FFMI)**. Le projet explore la corrélation entre les mesures corporelles (cou, poitrine, abdomen, hanches) et l'indice cible afin d'identifier les variables les plus prédictives.

### Objectifs principaux

<div align="left">

- **Identifier** les meilleures variables corporelles prédictives du FFMI
- **Construire** un modèle de régression linéaire robuste et interprétable
- **Traiter** les valeurs atypiques pour garantir la qualité des données
- **Visualiser** les corrélations et distributions via ggplot2

</div>

</td>
<td width="30%">

```mermaid
graph TD
    A[Données Brutes] --> B[Chargement]
    B --> C[Préparation & Nettoyage]
    C --> D[Modélisation]
    D --> E[Sélection du Modèle]
    E --> F[Interprétation FFMI]
    style A fill:#3B82F6
    style C fill:#10B981
    style D fill:#8B5CF6
    style F fill:#F59E0B
```

</td>
</tr>
</table>
</div>

### Variable Cible

<div align="center">

| Variable | Signification | Type |
|----------|---------------|------|
| **FFMI** | Fat-Free Mass Index — Indice de Masse Sans Graisse | Quantitative continue |

</div>

---

## Architecture du projet

<div align="center">

Le projet est organisé en **3 phases principales** correspondant au pipeline d'analyse statistique :

<br>

<table>
<thead>
<tr>
<th width="5%">#</th>
<th width="25%">Phase</th>
<th width="45%">Tâches réalisées</th>
</tr>
</thead>
<tbody>

<!-- PHASE 1 : CHARGEMENT -->
<tr>
<td colspan="3" align="center" style="background-color:#3B82F6; color:white;"><b>PHASE 1 : Chargement des données</b></td>
</tr>
<tr>
<td align="center"><b>1</b></td>
<td><b>Data Loading</b></td>
<td>
• Import du jeu de données des mesures corporelles<br>
• Inspection de la structure et des types de variables<br>
• Analyse descriptive initiale (min, max, moyenne, écart-type)
</td>
</tr>

<!-- PHASE 2 : PREPARATION -->
<tr>
<td colspan="3" align="center" style="background-color:#10B981; color:white;"><b>PHASE 2 : Préparation des données</b></td>
</tr>
<tr>
<td align="center"><b>2</b></td>
<td><b>Data Preparation</b></td>
<td>
• Détection et traitement des valeurs atypiques (outliers)<br>
• Vérification des hypothèses de normalité<br>
• Analyse des corrélations entre variables corporelles<br>
• Visualisation des distributions avec ggplot2
</td>
</tr>

<!-- PHASE 3 : MODELISATION -->
<tr>
<td colspan="3" align="center" style="background-color:#8B5CF6; color:white;"><b>PHASE 3 : Modélisation statistique</b></td>
</tr>
<tr>
<td align="center"><b>3</b></td>
<td><b>Modeling & Sélection</b></td>
<td>
• Construction de plusieurs modèles de régression linéaire<br>
• Exploration des variables : cou, poitrine, abdomen, hanches<br>
• Évaluation des modèles (R², RMSE, résidus)<br>
• Sélection du meilleur modèle prédictif<br>
• Interprétation des coefficients
</td>
</tr>

</tbody>
</table>

</div>

---

## Variables explorées

<div align="center">

<table>
<tr>
<td align="center" width="25%">
<h3>🔵 Cou</h3>
<img src="https://img.shields.io/badge/Mesure-Cou-3B82F6?style=flat-square" /><br><br>
<sub>Circonférence cervicale</sub>
</td>
<td align="center" width="25%">
<h3>🟢 Poitrine</h3>
<img src="https://img.shields.io/badge/Mesure-Poitrine-10B981?style=flat-square" /><br><br>
<sub>Tour de poitrine</sub>
</td>
<td align="center" width="25%">
<h3>🟣 Abdomen</h3>
<img src="https://img.shields.io/badge/Mesure-Abdomen-8B5CF6?style=flat-square" /><br><br>
<sub>Tour abdominal</sub>
</td>
<td align="center" width="25%">
<h3>🟡 Hanches</h3>
<img src="https://img.shields.io/badge/Mesure-Hanches-F59E0B?style=flat-square" /><br><br>
<sub>Tour de hanches</sub>
</td>
</tr>
</table>

</div>

---

## Métriques d'évaluation

<div align="center">

<table>
<tr>
<td align="center" width="33%">
<h3>Qualité du modèle</h3>
<img src="https://img.shields.io/badge/R²-Coefficient_de_détermination-3B82F6?style=for-the-badge" /><br>
<img src="https://img.shields.io/badge/R²_ajusté-Pénalisation_variables-3B82F6?style=for-the-badge" />
</td>
<td align="center" width="33%">
<h3>Erreur de prédiction</h3>
<img src="https://img.shields.io/badge/RMSE-Erreur_quadratique-10B981?style=for-the-badge" /><br>
<img src="https://img.shields.io/badge/Résidus-Distribution_&_analyse-10B981?style=for-the-badge" />
</td>
<td align="center" width="33%">
<h3>Hypothèses</h3>
<img src="https://img.shields.io/badge/Normalité-Test_Shapiro--Wilk-8B5CF6?style=for-the-badge" /><br>
<img src="https://img.shields.io/badge/Corrélation-Pearson-8B5CF6?style=for-the-badge" />
</td>
</tr>
</table>

</div>

---

## Stack Technologique

<div align="center">

<table>
<tr>
<td align="center" width="25%">
<h3>Langage</h3>
<img src="https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white" />
</td>
<td align="center" width="25%">
<h3>Visualisation</h3>
<img src="https://img.shields.io/badge/ggplot2-2C8EBB?style=for-the-badge&logoColor=white" />
</td>
<td align="center" width="25%">
<h3>Modélisation</h3>
<img src="https://img.shields.io/badge/Régression_Linéaire-10B981?style=for-the-badge&logoColor=white" />
</td>
<td align="center" width="25%">
<h3>Domaine</h3>
<img src="https://img.shields.io/badge/Statistiques-8B5CF6?style=for-the-badge&logoColor=white" />
</td>
</tr>
</table>

</div>

---

## Livrables du projet

<div align="center">

<table>
<thead>
<tr>
<th width="40%">Livrable</th>
<th width="25%">Format</th>
<th width="35%">Statut</th>
</tr>
</thead>
<tbody>
<tr>
<td><b>Script d'analyse complet</b></td>
<td>.R / .Rmd</td>
<td><img src="https://img.shields.io/badge/Obligatoire-critical?style=flat-square" /></td>
</tr>
<tr>
<td><b>Visualisations ggplot2</b></td>
<td>PNG / PDF</td>
<td><img src="https://img.shields.io/badge/Obligatoire-critical?style=flat-square" /></td>
</tr>
<tr>
<td><b>Modèle de régression final</b></td>
<td>.RData / .rds</td>
<td><img src="https://img.shields.io/badge/Obligatoire-critical?style=flat-square" /></td>
</tr>
<tr>
<td><b>Rapport d'analyse statistique</b></td>
<td>PDF / HTML (knitr)</td>
<td><img src="https://img.shields.io/badge/Obligatoire-critical?style=flat-square" /></td>
</tr>
</tbody>
</table>

</div>

---

## Contact

<div align="center">

Pour toute question concernant ce projet :

<table>
<tr>
<td align="center" width="50%">
<a href="https://github.com/EkiaND/">
<img src="https://ui-avatars.com/api/?name=Romain+Lesueur&size=150&background=8B5CF6&color=fff&bold=true&rounded=true" alt="Romain Lesueur" />
</a>
<br><br>
<h3>Romain Lesueur</h3>
<p>
<img src="https://img.shields.io/badge/Statistiques-ML-8B5CF6?style=flat-square" />
<img src="https://img.shields.io/badge/R-Developer-8B5CF6?style=flat-square" />
</p>
<sub>Modélisation statistique & Régression</sub>
</td>
</tr>
</table>

</div>

---

<div align="center">

### Informations du projet

**Projet de Statistiques — 2024**
*Modélisation de l'Indice de Masse Graisseuse par régression linéaire*

<br>

---

<!-- Footer avec vague -->
<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=100&section=footer" />

<div align="center">
<sub>© 2024 - Projet académique - Tous droits réservés</sub>
<br>
<sub>Romain Lesueur</sub>
</div>

</div>
