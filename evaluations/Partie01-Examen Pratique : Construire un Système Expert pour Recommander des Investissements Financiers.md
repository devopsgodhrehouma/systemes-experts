# **Examen Pratique Partie 01: Construire un Système Expert pour Recommander des Investissements Financiers**

---

#### **Introduction**

Bonjour à tous,  
Dans cet examen, vous allez **construire un système expert simple** qui recommande des investissements financiers en fonction du **revenu** et de la **tolérance au risque** des clients. 
Je vais vous guider pas à pas, mais il est essentiel de bien suivre chaque étape et de **réaliser les exercices demandés avec soin**.

---

### **Objectif de l'Exercice**

À la fin de cet exercice, vous devez :
1. Créer une **base de connaissances** dans Excel pour stocker les règles.
2. Implémenter un **moteur d’inférence** simple avec des formules Excel.
3. Tester et valider votre système avec différents scénarios.
4. Présenter clairement votre travail final.

---

### **Étape 1 : Comprendre le Contexte**

Un système expert fonctionne en imitant les décisions d’un expert humain. Ici, vous jouez le rôle d’un conseiller financier et devez aider un client à choisir un investissement en fonction :
1. **De son revenu mensuel** : Faible, Moyen, Élevé.
2. **De sa tolérance au risque** : Faible, Modérée, Élevée.

Voici les **trois types d'investissements possibles** :
- **Compte d’épargne** : Recommandé pour les clients ayant un faible revenu ou une faible tolérance au risque.
- **Obligations** : Recommandées pour une tolérance modérée et des revenus moyens ou élevés.
- **Actions** : Recommandées pour les clients à revenu élevé et aimant le risque.

#### **Règles à utiliser :**

| **Revenu**     | **Tolérance au risque** | **Recommandation**     |
|-----------------|-------------------------|-------------------------|
| Faible         | Faible                  | Compte d’épargne       |
| Moyen          | Modérée                 | Obligations            |
| Élevé          | Élevée                  | Actions                |
| Faible         | Modérée                 | Obligations            |
| Moyen          | Élevée                  | Actions                |
| Élevé          | Faible                  | Obligations            |

---

### **Étape 2 : Créer la Base de Connaissances**

1. **Ouvrez Excel** (ou Google Sheets si Excel n’est pas disponible).
2. **Créez un tableau** avec les colonnes suivantes :
   - **Revenu** : Faible, Moyen, Élevé.
   - **Tolérance au risque** : Faible, Modérée, Élevée.
   - **Recommandation** : Compte d’épargne, Obligations, Actions.
3. **Remplissez la table en suivant les règles ci-dessus.**

Exemple :

| Revenu   | Tolérance au Risque | Recommandation     |
|----------|---------------------|--------------------|
| Faible   | Faible              | Compte d’épargne   |
| Moyen    | Modérée             | Obligations        |
| Élevé    | Élevée              | Actions            |

---

### **Étape 3 : Implémenter un Moteur d’Inférence dans Excel**


1. Ajoutez une nouvelle feuille Excel appelée **Système** pour les entrées des clients :
   - **Colonne A** : Revenu.
   - **Colonne B** : Tolérance au risque.
   - **Colonne C** : Recommandation.

## Références pour vous aider :
- https://www.youtube.com/watch?v=yKjFm3Ijv0I&ab_channel=LaminuteExcel
- https://www.youtube.com/watch?v=oTV3ZGPLQuU&ab_channel=Bertrand.Tech

2. **Entrez une formule conditionnelle** dans la cellule C2 pour analyser les données et donner une recommandation :
   ```excel
   =SI(ET(A2="Faible";B2="Faible");"Compte d’épargne";
     SI(ET(A2="Moyen";B2="Modérée");"Obligations";
     SI(ET(A2="Élevé";B2="Élevée");"Actions";
     "Aucune recommandation")))
   ```

3. **Testez votre système** :
   - Entrez **Faible** dans la cellule A2 et **Faible** dans B2 → La cellule C2 doit afficher **Compte d’épargne**.
   - Changez les données (par exemple, **Moyen** et **Modérée**) pour vérifier que la recommandation change correctement.

4. Copiez la formule pour les autres lignes si vous avez plusieurs clients.

---

### **Étape 4 : Tester et Valider le Système**

#### Scénarios à Tester
Entrez les données suivantes dans votre système et vérifiez les résultats obtenus :

| **Revenu** | **Tolérance au Risque** | **Résultat Attendu**     |
|------------|-------------------------|--------------------------|
| Faible     | Faible                  | Compte d’épargne         |
| Moyen      | Modérée                 | Obligations              |
| Élevé      | Élevée                  | Actions                  |
| Faible     | Modérée                 | Obligations              |
| Moyen      | Élevée                  | Actions                  |
| Élevé      | Faible                  | Obligations              |

#### Vérifiez :
- Le système donne-t-il les **résultats corrects** pour chaque cas ?
- Si une erreur apparaît, corrigez vos formules ou vérifiez la table de règles.

---

### **Étape 5 : Présentation des Résultats**

1. Préparez une présentation avec les éléments suivants :
   - **Votre base de connaissances** (le tableau des règles dans Excel).
   - **Les résultats obtenus** pour chaque scénario.
   - Une explication simple de comment le système fonctionne (par exemple : "Le système utilise une formule pour comparer le revenu et la tolérance au risque du client avec les règles préprogrammées").

2. Expliquez :
   - Pourquoi ces règles ont été choisies.
   - Ce que vous avez appris en construisant le système.

---

### **Étape 6 : Activité Bonus**

1. Si vous avez terminé rapidement, essayez de **visualiser votre base de connaissances** avec un outil de carte mentale comme FreeMind.
   - Créez un nœud principal appelé **Recommandation d’investissements**.
   - Ajoutez des sous-nœuds pour chaque règle, par exemple :
     - **Revenu : Faible → Tolérance : Faible → Compte d’épargne**.
     - **Revenu : Élevé → Tolérance : Élevée → Actions**.
2. Partagez cette carte mentale avec vos collègues ou votre professeur.

---

### **Barème d’Évaluation**
1. **Base de Connaissances (5 points)** :
   - La table des règles est complète et bien structurée.
2. **Moteur d’Inférence (5 points)** :
   - Les formules fonctionnent correctement et donnent des recommandations précises.
3. **Tests et Validation (5 points)** :
   - Tous les scénarios sont testés et les résultats sont justes.
4. **Présentation (5 points)** :
   - Explication claire et organisation des résultats.

---

### **Conclusion**

Cet exercice vous a permis de :
1. Comprendre comment fonctionnent les systèmes experts.
2. Construire un système expert simple avec Excel.
3. Tester et valider les recommandations.

