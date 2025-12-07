# Ma prédiction - Exercice 07

## Traçage ligne par ligne

**Lignes 3-4 :** Initialisation

- nombre = 10
- tableau = {1, 2, 3}

**Lignes 6-7 :** Affichages "Avant"

```
Avant : nombre = 10
Avant : tableau[0] = 1
```

---

### Appel : `modifierNombre(nombre)` (ligne 9)

**Dans la fonction :**

- n reçoit une COPIE de nombre : n = 10
- n = n + 100 → n = 10 + 100 = 110
- Affichage :
  ```
  Dans modifierNombre : n = 110
  ```

**Question : `nombre` dans main a-t-il changé ?** non

---

### Appel : `modifierTableau(tableau)` (ligne 10)

**Dans la fonction :**

- tab reçoit une RÉFÉRENCE vers le même tableau
- tab[0] = tab[0] + 100 → tab[0] = 101
- Affichage :
  ```
  Dans modifierTableau : tab[0] = 101
  ```

**Question : `tableau[0]` dans main a-t-il changé ?** oui

---

**Lignes 12-13 :** Affichages "Après"

- nombre = 10 (modifié ou pas ?) pas modifié
- tableau[0] = 101 (modifié ou pas ?) modifié

```
Apres : nombre = 10
Apres : tableau[0] = 101
```

---

### Appel : `doubler(nombre)` avec affectation (ligne 15)

- doubler(10) retourne : 20
- nombre = 20 (réaffecté avec la valeur de retour)

**Ligne 16 :** Affichage

```
Apres doubler : nombre = 20
```

---

## Question finale

Pourquoi `modifierNombre` n'a pas changé `nombre` mais `modifierTableau` a changé `tableau[0]` ?

Réponse : `modifierNombre` ne return pas `nombre`, il l'a modifie dans sa fonction avec une copie de `nombre`.
`modifierTableau` a changé `tableau[0]` car il utilise directement sans faire de copie donc modifie directement le contenue de `tableau[0]`.
