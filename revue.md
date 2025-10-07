# Règles de Validation des Projets Inventaire

## Section 1 : Standards de Code Généraux

### 1.1 Nommage
- **Noms des variables, fonctions, et classes en français**
- **Noms des variables, fonctions, et inner classes en français** avec les accents
- Utiliser la nomenclature française cohérente dans tout le projet

### 1.2 Formatage et Indentation
- **Indentation : 2 espaces uniquement**
- **Jamais utiliser de tabulations**
- **Ligne vide entre les sections de code** pour séparer les blocs logiques
- **Unifier l'espacement** entre les lignes de même section (soit toutes avec ligne vide, soit aucune)
- **Pas d'espaces à la fin des lignes**

### 1.3 Organisation des Imports
- **Ordre des imports** (du plus généralisé au plus particulier) :
  1. `java.*`
  2. `org.jetbrains.exposed.*`
  3. `org.kopi.galite.*`
  4. `org.kopi.zembra.*`
  5. `com.progmag.pdv.*`
- **Ligne vide entre les imports** de packages différents

### 1.4 En-têtes et Documentation
- **Ajouter l'en-tête de copyright** complet
- **Vérifier le propset Id du fichier** (format : `$Id: NomFichier.kt XXX YYYY-MM-DD HH:MM:SSZ utilisateur $`)
- **Commentaires clairs et en français**

### 1.5 Formatage des Arguments
- Si tous les arguments sauf le premier sur une ligne séparée, les arguments commencent à la position du premier argument

## Section 2 : TransDB et DBSchema

### 2.1 Traçabilité
- **Définir les tables dans TransDB** lors de la création pour la traçabilité

### 2.2 Formatage DBSchema et TransDB
- **Symbole égal à la position 41** dans les fichiers DBSchema et TransDB
- **Noms des tables et colonnes en minuscules**
- **Ordre des tables dans DBSchema : alphabétique**

### 2.3 Validation des Tables
- **Vérifier les colonnes des tables** (exemple : nombre de caractères dans varchar)
- **Vérifier les références** entre tables

## Section 3 : Formulaires et Rapports

### 3.1 Commandes et Navigation
- **Vérifier les commandes** (breakCommand, report, etc.)
- **Vérifier les index** des tables
- **Vérifier le nombre de lignes des blocs**

### 3.2 Positionnement des Champs
- **Vérifier les positions des fields** (at(x, y))
- **Vérifier les jointures** (INNER JOIN, LEFT JOIN, RIGHT JOIN)
- **Vérifier les domaines des fields** (STRING, INT, domaines personnalisés)
- **Ordre des champs de création/modification** :
  1. `creePar`
  2. `creeLe`
  3. `modifiePar`
  4. `modifieLe`

### 3.3 Utilisation de Galite
- **Utiliser Galite dans tous les cas possibles** (pas de redéfinition non nécessaire)
- **Privilégier les domaines Galite** aux types primitifs quand approprié

### 3.4 Structure des Rapports
- **Gestion des valeurs nulles** avec `?: ""` pour les champs STRING

## Section 4 : Global.kt

### 4.1 Configuration des Domaines
- **Vérifier les largeurs** des domaines
- **Noms en pluriels** pour les domaines
- **Vérifier si ListDomain ou CodeDomain** est approprié
- **Vérifier si Convert (UPPER/LOWER)** est nécessaire

## Section 5 : Tests et Scénarios

### 5.1 Scénarios de Validation
- **Affichage** : vérifier que les données s'affichent correctement
- **Insertion** : tester l'ajout de nouveaux enregistrements
- **Suppression** : tester la suppression d'enregistrements
- **Modification** : tester la mise à jour d'enregistrements (avec différent utilisateur)

### 5.2 Tests Fonctionnels
- **Rapports** : vérifier que les rapports génèrent les bonnes données
- **Filtres** : tester les critères de recherche

## Section 6 : Checklist de Validation

### 6.1 Avant Validation
- [ ] Tous les fichiers compilent sans erreur
- [ ] Aucun warning critique
- [ ] En-têtes de copyright présents
- [ ] Propset Id corrects

### 6.2 Validation du Code
- [ ] Noms en français avec accents
- [ ] Indentation 2 espaces (pas de tabs)
- [ ] Imports organisés et séparés
- [ ] Commentaires en français
- [ ] Formatage des arguments respecté

### 6.3 Validation Base de Données
- [ ] Tables définies dans TransDB
- [ ] Noms en minuscules
- [ ] Références correctes
- [ ] Ordre alphabétique des tables
- [ ] Champs de traçabilité dans le bon ordre

### 6.4 Validation Formulaires/Rapports
- [ ] Commandes présentes
- [ ] Positions des champs correctes
- [ ] Jointures appropriées
- [ ] Domaines Galite utilisés
- [ ] Gestion des valeurs nulles

### 6.5 Validation Global.kt
- [ ] Widths appropriées
- [ ] Noms en pluriels
- [ ] Type de domaine correct (ListDomain/CodeDomain)
- [ ] Convert si nécessaire

### 6.6 Tests Fonctionnels
- [ ] Affichage fonctionne
- [ ] Insertion fonctionne
- [ ] Suppression fonctionne
- [ ] Modification fonctionne
- [ ] Rapports génèrent les bonnes données

---

**Note** : Ce document doit être utilisé comme référence pour valider tous les projets du module inventaire. Chaque section doit être vérifiée avant la mise en production.
