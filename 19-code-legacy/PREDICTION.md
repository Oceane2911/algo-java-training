# Ma prédiction - Exercice 19

## Partie 1 : Comprendre l'existant

### Classe `Produit`

**Attributs (noms cryptiques) :**
- `n` représente : nom du produit
- `p` représente : prix du produit
- `q` représente : quantite

**Méthode `valeur()` :**
- Que calcule-t-elle ? prix * quantite = prix total de produit

---

### Classe `Inventaire`

**Attributs :**
- `prods` représente : tableau des produits
- `nb` représente : nombre de produit

**Méthodes :**
- `ajouter(Produit p)` : ajout un produit a la fin du tableau 
- `chercher(String nom)` : cherche un produits dans le tableau
- `afficher()` : affiche le produit en fonction du nom du produit, du prix et de la quantite 
- `valeurTotale()` : calcule la valeur total des produits dans le tableau prods

---

## Partie 2 : Prédire la sortie actuelle

```
=== Inventaire ===
Pomme : 2.50 x 100
Pain : 1.20 x 50
Lait : 0.95 x 75
Beurre : 2.10 x 30

=== Recherche 'Pain' ===
Trouve : Pain a 1.20 euros

=== Valeur totale ===
Valeur : 444.25 euros

```

---

## Partie 3 : Ajouter la fonctionnalité

**Fonctionnalité demandée :** 
Ajouter une méthode `afficherCher(double seuil)` qui affiche les produits dont le prix est supérieur au seuil.

**Ma méthode :**
```java
public void afficherCher(double seuil) {
   for( int i = 0; i < nb; i++){
    if(prods[i].getPrix()> seuil){
        System.out.println("Le prix de " + prods[i].getNom() + " est supérieur à " + seuil)
    }
   } 
}
```

**Sortie attendue pour `afficherCher(2.0)` :**
```
=== Produits chers (>2 euros) ===
Le prix de Pomme est supérieur à 2 euros.
Le prix de Beurre est supérieur à 2 euros.
```
