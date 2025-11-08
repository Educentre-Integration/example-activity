# Intégration avec Educentre

### Activités pédagogiques

Intégrez vos jeux et vos applications pour apprenants avec Educentre 

**1. Intégrer le `bridge` Educentre dans votre application**

```html
<script src="https://cdn.jsdelivr.net/gh/educentre-integration/libraries@latest/activity/bridge.min.js"></script>
```

**2. Utiliser le `bridge` pour récupérer des informations ou envoyer des informations à Educentre**

Vous pouvez utiliser le `bridge` dans l'espace apprenant comme dans l'espace contributeur. Utilisez le dans l'espace apprenant lorsque les apprenants utilisent votre activité pour récupérer, sauvegarder des données ou même envoyer une note. Vous pouvez également l'utiliser dans l'espace contributeur pour enregistrer des paramètres généraux qui seront appliqués à tous les apprenants.

```js
const edac = new EducentreActivity();

/* ===================================================
Espace APPRENANT : vous pouvez lire et enregistrer des données pour un groupe entier.
Les réponses respectent l'interface suivante :
interface EducentreStorageResponse {
    token: string;
    student: {
        fullname?: string;
    };
    certificationStorage?: any;
}
*/
edac.getStorage((response) => {
    console.log(response);
});

const storage = ...;
edac.saveStorage(storage, (response) => {
    console.log(response);
});

// Espace APPRENANT : vous pouvez soumettre une note à une évaluation sur Educentre. La note doit être comprise entre 0 et 1.
const score = 0.8; // Equivalent de 16 sur 20
edac.sendScore(score);

/* ===================================================
Espace CONTRIBUTEUR : dans la console de l'activité pédagogique, vous pouvez enregistrer des paramètres généraux grâce à la configuration
*/
edac.getConfiguration((response) => {
    console.log(response);
});
edac.saveConfiguration(configuration, (response) => {
    console.log(response);
});
```
