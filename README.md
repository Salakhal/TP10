# TP 10 : Collections

##  Objectif général
Ce TP a pour but de maîtriser l’utilisation des principales **collections Java** (`List`, `Set`, `Map`) à travers une série d’exercices progressifs.  
Chaque exercice introduit une structure de collection différente et illustre son usage dans des cas concrets.

##  Exercice 1 : Gestionnaire de Liste de Courses avec List)

###  Objectifs pédagogiques
- Comprendre la structure dynamique d’une `ArrayList`
- Ajouter, supprimer et parcourir des éléments
- Manipuler les collections via les boucles et les itérateurs

  ## Sortie attendue
```
Gestion de la liste de courses

Commandes : add, remove, find, show, exit
Entrez une commande : add
Article à ajouter : Lait
'Lait' ajouté.

Commandes : add, remove, find, show, exit
Entrez une commande : add
Article à ajouter : Pain
'Pain' ajouté.

Commandes : add, remove, find, show, exit
Entrez une commande : show

Votre liste de courses :
 1. Lait
 2. Pain

Commandes : add, remove, find, show, exit
Entrez une commande : find
Article à rechercher : Oeufs
'Oeufs' n'est pas dans la liste.

Commandes : add, remove, find, show, exit
Entrez une commande : remove
Article à supprimer : Pain
'Pain' supprimé.

Commandes : add, remove, find, show, exit
Entrez une commande : show

Votre liste de courses :
 1. Lait

Commandes : add, remove, find, show, exit
Entrez une commande : exit
Au revoir !
 
```

<img width="557" height="957" alt="image" src="https://github.com/user-attachments/assets/9cd414f0-6ef0-4c9b-9915-5a10d6e7ee03" />


  

  ## Exercice 2 – Gestionnaire de mots uniques (Set)

###  Objectifs
- Utiliser `HashSet`, `LinkedHashSet` et `TreeSet`
- Stocker des mots uniques extraits d’un texte
- Comparer les ordres (aléatoire, insertion, alphabétique)
- Proposer des opérations de recherche et de suppression

###  Classe principale : `WordManager.java`

- Parse un texte brut en mots (minuscules, sans ponctuation)
- Alimente simultanément :
  - `HashSet` : performances rapides
  - `LinkedHashSet` : ordre d’insertion
  - `TreeSet` : ordre naturel (alphabétique, insensible à la casse)
- Fournit :
  - `contains(String word)` : vérifie la présence
  - `remove(String word)` : supprime le mot de tous les ensembles
  - `displayAll()` : affiche les trois ensembles
 
   ##  Contexte
L’exercice consiste à :
1. Charger un jeu de données textuelles
2. Préparer les données pour la classification (tokenisation, vectorisation)
3. Entraîner plusieurs modèles de classification
4. Combiner les prédictions via un vote majoritaire
5. Évaluer la précision et la performance des modèles


 ## Sortie attendue
```
=== Toutes les tâches ===
[1] (prio=2) PENDING — Écrire la doc
[2] (prio=1) PENDING — Corriger les bugs
[3] (prio=3) PENDING — Préparer démo
[4] (prio=4) PENDING — Envoyer emails

=== Trier par priorité ===
[2] (prio=1) PENDING — Corriger les bugs
[1] (prio=2) PENDING — Écrire la doc
[3] (prio=3) PENDING — Préparer démo
[4] (prio=4) PENDING — Envoyer emails

=== Tâche #2 en cours ===
[2] (prio=1) IN_PROGRESS — Corriger les bugs
[1] (prio=2) PENDING — Écrire la doc
[3] (prio=3) PENDING — Préparer démo
[4] (prio=4) PENDING — Envoyer emails

=== Filtrer PENDING ===
[1] (prio=2) PENDING — Écrire la doc
[3] (prio=3) PENDING — Préparer démo
[4] (prio=4) PENDING — Envoyer emails

=== Supprimer tâche #1 ===
[2] (prio=1) IN_PROGRESS — Corriger les bugs
[3] (prio=3) PENDING — Préparer démo
[4] (prio=4) PENDING — Envoyer emails
```
 <img width="636" height="694" alt="image" src="https://github.com/user-attachments/assets/784e6cc6-cc2b-45e5-94c0-dad1bde56027" />
 


## Exercice 3 : Maîtrise des Set : Gestionnaire de Mots Uniques

##  Objectifs pédagogiques
- Maîtriser l’utilisation des trois implémentations de `Set` en Java :
  - `HashSet` : performance optimale (O(1)), ordre indéfini
  - `LinkedHashSet` : performance similaire, conserve l’ordre d’insertion
  - `TreeSet` : trie automatique des éléments (ordre naturel ou selon un Comparator)
- Extraire et stocker des mots uniques à partir d’un texte
- Comparer l’affichage des mots selon les trois types de `Set`
- Rechercher et supprimer des mots dans les collections

---

##  Contexte
À partir d’un texte brut, l’application :
1. Parse le texte en mots (minuscules, sans ponctuation)
2. Alimente simultanément un `HashSet`, un `LinkedHashSet` et un `TreeSet`
3. Affiche le contenu de chaque ensemble pour comparer les ordres
4. Permet de rechercher ou supprimer un mot via l’utilisateur

---
 ## Exemple d’exécution :
 
<img width="1671" height="718" alt="image" src="https://github.com/user-attachments/assets/c482bd42-4f51-4cba-be33-8ef6ca82f065" />


## Exercice 4 : Gestion d’un Dictionnaire Bilingue avec Map


##  Objectifs pédagogiques
- Maîtriser l’utilisation des trois implémentations de `Map` en Java :
  - `HashMap` : accès rapide sans ordre garanti
  - `LinkedHashMap` : conserve l’ordre d’insertion
  - `TreeMap` : trie automatique des clés (ordre alphabétique)
- Gérer un dictionnaire bilingue avec ajout, mise à jour, recherche et suppression
- Utiliser les Streams pour rechercher par préfixe (autocomplétion)
- Comparer les comportements des différentes implémentations de `Map`

---

##  Contexte
L’application DictionaryManager permet :
1. Ajouter et mettre à jour des entrées anglais → français
2. Rechercher une traduction exacte
3. Supprimer une entrée
4. Afficher toutes les entrées selon HashMap, LinkedHashMap ou TreeMap
5. Rechercher les entrées par préfixe (insensible à la casse) pour autocomplétion

---

 ## Sortie attendue
```
=== HashMap (unordered) ===
banana     → banane
date       → datte
apricot    → abricot
apple      → pomme
cherry     → cerise

=== LinkedHashMap (insertion order) ===
apple      → pomme
banana     → banane
cherry     → cerise
date       → datte
apricot    → abricot

=== TreeMap (alphabetical order) ===
apple      → pomme
apricot    → abricot
banana     → banane
cherry     → cerise
date       → datte

Mot à traduire : apple
Traduction de 'apple' : pomme

Préfixe à chercher : ap
Résultats pour "ap" :
apple      → pomme
apricot    → abricot

Mot à supprimer : banana
'banana' supprimé avec succès.

=== HashMap (unordered) ===
date       → datte
apricot    → abricot
apple      → pomme
cherry     → cerise

=== LinkedHashMap (insertion order) ===
apple      → pomme
cherry     → cerise
date       → datte
apricot    → abricot

=== TreeMap (alphabetical order) ===
apple      → pomme
apricot    → abricot
cherry     → cerise
date       → datte

```
<img width="570" height="1238" alt="image" src="https://github.com/user-attachments/assets/deff2d88-7f2f-4021-9f16-9066cfaa46c9" />

## Exercice 5 : Maîtrise des Collections – Gestion d’une bibliothèque

##  Objectifs pédagogiques
- Maîtriser l’utilisation des principales collections Java :
  - `List` (ArrayList) pour stocker les livres
  - `Map` pour suivre le stock et les emprunts
  - `Set` pour gérer les doublons si nécessaire
- Comprendre quand utiliser `ArrayList`, `HashMap` ou `HashSet`
- Manipuler ajout, suppression, recherche et itération sur les collections
- Structurer un projet Java avec plusieurs classes collaborant via des collections

---

##  Contexte
L’application permet de gérer une bibliothèque :
1. Stocker des livres identifiés par ISBN, titre et auteur
2. Suivre la quantité disponible pour chaque livre
3. Enregistrer les prêts des usagers
4. Gérer les retours et l’état du stock
5. Prévenir les doublons d’emprunts

---

 ## Sortie attendue
```
Disponibles : [Effective Java (ISBN:978-0134685991) by Joshua Bloch, Head First Java (ISBN:978-0596009205) by Kathy Sierra]
Alice emprunte Effective Java : true
Bob emprunte Effective Java : true
Bob emprunte Effective Java à nouveau : false
Disponibles : [Effective Java (ISBN:978-0134685991) by Joshua Bloch]
Emprunts d'Alice : [Effective Java (ISBN:978-0134685991) by Joshua Bloch]
Emprunts de Bob   : [Effective Java (ISBN:978-0134685991) by Joshua Bloch]
Alice retourne le livre : true
Disponibles après retour : [Effective Java (ISBN:978-0134685991) by Joshua Bloch, Head First Java (ISBN:978-0596009205) by Kathy Sierra]


```

<img width="1636" height="299" alt="image" src="https://github.com/user-attachments/assets/3b739ad7-7449-4240-af17-d2c927126b2f" />





