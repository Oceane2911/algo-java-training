# Ma prédiction - Exercice 17

## Fonction `moyenneInef`

**Problème identifié :** la 1er boucle est inutile 

**Nombre d'opérations actuelles (pour n éléments) :** On prend une valeur i, on initialise la variable somme à 0, puis on parcourt j dans une boucle jusqu’à ce que j = i = 0. Ensuite, on incrémente i, on réinitialise somme à 0 et on boucle à nouveau jusqu’à j = i = 1, et ainsi de suite… On continue en incrémentant i, en réinitialisant somme et en bouclant jusqu’à j = i = n.

**Version optimisée :**
```java
public static double moyenneEff(int[] t) {
    double somme = 0;
    for( int i =0; i< t.length; i++){
        somme = somme + t[i];
    }
    return somme /t.length
}
```

---

## Fonction `contientDoublonInef`

**Problème identifié :** on ne peut rentrer dans la 1ère condition car i = 0 et j= 0 alors i et j sont pareil donc la 2ème patie de la condition ne seras pas verifie

**Version optimisée :**
```java
public static boolean contientDoublonEff(int[] t) {
    for (int i = 0; i < t.length; i++) {
            for (int j = 1; j < t.length; j++) {
                if (t[i] == t[j]) {
                    return true;
                }
            }
        }
        return false;
}
```

---

## Fonction `premierEtDernierInef`

**Problème identifié :** la premier boucle est inutile et le break feras arrete toute la fonction donc on n'aura le dernier

**Version optimisée :**
```java
public static String premierEtDernierEff(int[] t) {
    int premier = t[0];
    int dernier = t[t.length-1];
    return premier + " et " + dernier;
}
```

---

## Fonction `rechercheInef`

**Problème identifié :** boucle continue même si on a trouvé une valeur

**Version optimisée :**
```java
public static int rechercheEff(int[] t, int val) {
    int index = -1;
    for (int i = 0; i < t.length; i++) {
        if (t[i] == val) {
            index = i;
            return index;
        }
    }
    return index;
}
```
