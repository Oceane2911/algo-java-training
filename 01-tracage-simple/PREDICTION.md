# Ma prédiction - Exercice 01

## Traçage ligne par ligne

**Ligne 3 :** `int a = 5;`
- État : a = 5

**Ligne 4 :** `int b = 10;`
- État : a = 5, b = 10

**Ligne 5 :** `int c = a + b;`
- Calcul : 5 + 10 = c
- État : a = 5, b = 10, c = 15

**Lignes 7-9 :** Affichages
```
a = 5
b = 10
c = 15
```

**Ligne 11 :** `a = a + 3;`
- Calcul : 5 + 3 = a
- État : a = 8, b = 10, c = 18

**Ligne 12 :** `b = b - 2;`
- Calcul : 10 - 2 = 8
- État : a = 8, b = 8, c = 16

**Ligne 13 :** `c = a * b;`
- Calcul : 8 * 8 = 64
- État : a = 8, b = 8, c = 64

**Lignes 15-18 :** Affichages
```
Après modification :
a = 8
b = 8
c = 64
```

**Ligne 20 :** `int resultat = c / a;`
- Calcul : 64 / 8 = 8
- État : a = 8, b = 8, c = 64, resultat = 8

**Ligne 21 :** Affichage final
```
resultat = 8
```


