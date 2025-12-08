# Ma prédiction - Exercice 18

## Architecture

**Classes présentes :**
- Main → appelle les autre classe pour gérer et créer l'interface
- Banque → classe qui créer le nom, nombre de client et la créer d'un nouveux objet Client
- Client →  classe ayant un nom et un instance de Compte
- Compte → s'occupe du solde 

**Qui contient quoi ?**
- Banque contient : un constructeur avec le nom en privée, une instante d'une liste de client et un nombre de client de compte prive. Une fonction permet d'ajouter un clients a la liste, une autre permet d'affiche les info d'un client et une dernier permet de savoir le montant total d'argent a la banque.

- Client contient : un constructeur avec le nom du client en privée et une instance de compte prive, une fonction pour recupere le nom et une autre pour recupere le solde du compte du client, une autre pour deposer un montant sur notre compte, une autre fonction pour retirer un montant de notre compte et un derniere fonction pour transferer de l'argent à une autre personne

- Compte contient : un constructeur avec int solde privée, une fonction pour récupérer le solde, une autre pour ajouter un montant a notre solde et une autre pour retirer un montant de notre solde

---

## Traçage de l'exécution

### Création des objets

**Ligne 3 :** `new Banque("MaBanque")`
- Crée une Banque avec clients[] vide

**Lignes 5-6 :** `new Client(...)`
- Alice créé avec un Compte (solde = 0)
- Bob créé avec un Compte (solde = 0)

**Lignes 8-9 :** `ajouterClient(...)`
- clients[0] = alice, nbClients = 1
- clients[1] = bob, nbClients = 2

---

### Dépôts

**Ligne 11 :** `alice.deposer(100)`
- Appelle compte.crediter(100)
- Alice.compte.solde = 100

**Ligne 12 :** `bob.deposer(50)`
- Bob.compte.solde = 50

---

### Affichage initial

```
alice : 100
bob : 50
```

---

### Transfert

**Ligne 17 :** `alice.transferer(bob, 30)`

Que se passe-t-il dans transferer() ?
1. `this.retirer(30)` → Alice.compte.solde = 100-30=70
2. `destinataire.deposer(30)` → Bob.compte.solde = 50 +30 = 80

---

### Affichage après transfert

```
alice : 70
bob : 80
```

---

### Total en banque

**Ligne 22 :** `banque.totalDepots()`
- total = 70 + 80 = 150

```
Total :150
```
