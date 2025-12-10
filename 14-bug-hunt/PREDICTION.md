# Ma prédiction - Exercice 14

## BUG 1 : fonction `moyenne`

**Ligne suspecte :** 28

**Description du bug :** i = 6

**Ce qui va se passer :** i ne paut pas être egale a 6 car le tableau ne possede pas d'index 6

**Correction proposée :** i < t.length

---

## BUG 2 : fonction `estTrie`

**Ligne suspecte :** 36

**Description du bug :** pour la derniere itération t[5] ne peut exite car t.length = 5

**Ce qui va se passer :** erreur de java car index > longueur du tableau

**Correction proposée :** i<t.length-1>

---

## BUG 3 : fonction `inverse`

**Ligne suspecte :** 48

**Description du bug :** en prenant l'index t.length-1-i, dans les dernières itérations, on reprend un index qu'on avait déjà modifié

**Ce qui va se passer :** notre tableau ne va pas etre inverse

**Correction proposée :** double for imbrique

---

## BUG 4 : fonction `compter`

**Ligne suspecte :** 59

**Description du bug :** avec le return dans le if la fonction va s'arrete des la première occurence

**Ce qui va se passer :** count seras egale à 1

**Correction proposée :** enlever le return du if et de la boucle
