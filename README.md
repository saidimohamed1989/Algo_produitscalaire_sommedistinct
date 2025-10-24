# Problèmes Algorithmiques avec Tableaux et Vecteurs

Ce dépôt contient les solutions à deux problèmes algorithmiques utilisant des **tableaux** et des **vecteurs** en JavaScript.

---

## Problème 1 : Somme des éléments distincts entre deux ensembles

**Énoncé :**  
Étant donné deux ensembles d'éléments, trouvez la somme de tous les éléments **distincts** présents dans l’un ou l’autre des ensembles.  

**Exemple :**  
- Ensemble 1 : `[3, 1, 7, 9]`  
- Ensemble 2 : `[2, 4, 1, 9, 3]`  
- Résultat attendu : `13` (éléments distincts : 2, 4, 7)

**Solution (JavaScript) :**
```javascript
function sommeDistincte(tab1, tab2) {
    let somme = 0;

    for (let e of tab1) {
        if (!tab2.includes(e)) {
            somme += e;
        }
    }

    for (let e of tab2) {
        if (!tab1.includes(e)) {
            somme += e;
        }
    }

    return somme;
}

// Test
const ensemble1 = [3, 1, 7, 9];
const ensemble2 = [2, 4, 1, 9, 3];
console.log(sommeDistincte(ensemble1, ensemble2)); // Résultat : 13
