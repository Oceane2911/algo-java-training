# Ma prédiction - Exercice 11

## Analyse des fonctions

### Fonction `xxx(int[] t)`

**Que fait cette fonction ?**

- Analyse le code ligne par ligne :
  - r = t[0] → 3
  - Boucle : si t[i] > r alors r = t[i] → vérifie si t[i]>r alorsi ouis r prend la valeur de t[i] sinon il garde la valeur de t[i] précédent
  - return r → return int à la fin de la boucle

**En une phrase, cette fonction :** cette fonction permet de cherche le int le plus grand du tableau

**xxx({3, 7, 2, 9, 1, 5}) = 9**

---

### Fonction `yyy(int[] t)`

**Que fait cette fonction ?**

- Analyse :
  - r = 0 → r est initialiser à 0
  - Boucle : r = r + t[i] → ajoute à r la valeur de t[i] à chaque augmentation de i
  - return r → renvoie r à la fin de la boucle

**En une phrase, cette fonction :** cette fonction permet d'addictionner tous les valeurs du tabeau t

**yyy({3, 7, 2, 9, 1, 5}) = 27**

---

### Fonction `zzz(int[] t, int v)`

**Que fait cette fonction ?**

- Première boucle : compte les éléments où t[i] < v → 3
- Crée un nouveau tableau de taille c → tableau de 3 element
- Deuxième boucle : remplit le tableau avec les éléments < v → mettre la valeur de t[i] dans le nouveu tableau à l'index j si t[i]< v

**En une phrase, cette fonction :** cette fonction permet de renvoyer un nouveau tableau dans lequel se trouve toute les valeurs plus petite que la valeur v

**zzz({3, 7, 2, 9, 1, 5}, 4) = {3,2,1}**

---

### Fonction `aaa(int[] t)`

**Que fait cette fonction ?**

- Double boucle imbriquée → parcours le tableau t en reduissant la taille du tableau à chaque boucle fini.
  1ere itération: i = 0 => j prendra la valeur 0, 1 ,2, 3, 4 2eme itération: i = 1 => j prendra la valeur 0, 1 ,2, 3 etc
- Compare t[j] et t[j+1], échange si t[j] > t[j+1] → compare la valeur du tableau a l'index j avec la valeur suivante alors si la condiction est respecte tmp prend lla valeur de t[j], t[j] prend la valeur t[j+1] et t[j+1] prend la valeur tmp.

**En une phrase, cette fonction :** cette fonction permet de trier le tableau dans l'ordre croissant

**Après aaa({3, 7, 2, 9, 1, 5}) : {1, 2, 3, 5, 7, 9}**
