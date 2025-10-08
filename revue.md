# Revue de dossier APPS-02XX

## Section 1 : Standards de Code Généraux
- [ ] Noms des variables, fonctions, et classes en français
- [ ] Noms des variables, fonctions, et inner classes en français avec les accents
- [ ] Indentation 2 espaces uniquement (jamais de tabulations)
- [ ] Ligne vide entre les sections de code
- [ ] Unifier l'espacement entre les lignes de même section
- [ ] Pas d'espaces à la fin des lignes
- [ ] Ordre des imports respecté (java > exposed > galite > zembra > pdv)
- [ ] Ligne vide entre les imports de packages différents
- [ ] En-tête de copyright complet
- [ ] Propset Id du fichier correct
- [ ] Commentaires clairs et en français
- [ ] Formatage des arguments respecté

## Section 2 : TransDB et DBSchema
- [ ] Tables définies dans TransDB pour la traçabilité
- [ ] Symbole égal à la position 41 dans les fichiers DBSchema et TransDB
- [ ] Noms des tables et colonnes en minuscules
- [ ] Ordre des tables dans DBSchema alphabétique
- [ ] Colonnes des tables vérifiées (nombre de caractères dans varchar)
- [ ] Références entre tables vérifiées

## Section 3 : Formulaires et Rapports
- [ ] Commandes vérifiées (breakCommand, report, etc.)
- [ ] Index des tables vérifiés
- [ ] Nombre de lignes des blocs vérifié
- [ ] Positions des fields vérifiées (at(x, y))
- [ ] Jointures vérifiées (INNER JOIN, LEFT JOIN, RIGHT JOIN)
- [ ] Domaines des fields vérifiés (STRING, INT, domaines personnalisés)
- [ ] Ordre des champs de création/modification respecté (creePar, creeLe, modifiePar, modifieLe)
- [ ] Galite utilisé dans tous les cas possibles
- [ ] Gestion des valeurs nulles avec `?: ""` pour les champs STRING

## Section 4 : Global.kt
- [ ] Largeurs des domaines vérifiées
- [ ] Noms en pluriels pour les domaines
- [ ] Type de domaine approprié (ListDomain ou CodeDomain)
- [ ] Convert (UPPER/LOWER) si nécessaire

## Section 5 : Tests et Scénarios
- [ ] Affichage
- [ ] Insertion
- [ ] Suppression
- [ ] Modification (avec différent utilisateur)
- [ ] Rapports : génèrent les bonnes données
- [ ] Filtres : critères de recherche fonctionnent

