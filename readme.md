# Activité Pédagogique

## Structure d'une Activité Pédagogique

Une activité pédagogique se compose de plusieurs pages, dont une est obligatoire et les autres optionnelles.

### Partie Apprenant (Obligatoire)
La forme minimale d'une activité est une page unique destinée à l'apprenant. C'est cette page qui s'affiche dans l'iframe. Elle constitue le cœur de l'activité, la partie "jeu" ou exercice interactif pour l'étudiant.

### Partie Contributeur (Optionnelle)
Il existe deux pages supplémentaires destinées aux contributeurs (créateurs ou administrateurs de l'activité) :

1.  **La Console** : Cette page permet au contributeur ou à l'admin de suivre la progression des apprenants en temps réel.
2.  **La Configuration** : Cette page permet de configurer l'activité pédagogique. Elle est utile pour adapter une même activité (code source) à des contextes différents (par exemple, des exercices de code différents).
    *   Elle permet de créer et sauvegarder une configuration spécifique (au format JSON) propre à la formation.

## Stockage et Multijoueur
La progression et les données de l'activité sont stockées dans un espace de stockage (Storage).
*   **Stockage partagé** : Il n'y a qu'un seul stockage pour tous les apprenants d'un même groupe ou d'une même promotion.
*   **Multijoueur** : Ce partage est essentiel pour les activités multijoueurs, où les actions d'un apprenant peuvent affecter les autres (par exemple, leurs points de vie).

## Sécurité et Offuscation
Des fonctions sont disponibles pour offusquer et dé-offusquer les données.
*   **Objectif** : Prévenir la triche.
*   **Fonctionnement** : Si l'on utilise le `localStorage` par exemple, l'offuscation rend les données difficilement lisibles et modifiables par l'apprenant, sécurisant ainsi la progression ou le score.

## Documentation
Pour en savoir plus sur l'API, consultez la documentation officielle : [Educentre Activity Bridge](https://github.com/Educentre-Integration/libraries).

