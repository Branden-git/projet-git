# projet-git

1. Branche main
- C’est la branche **principale**, celle qu’on protège généralement et qu’on déploie en production.
- Elle ne contient que du **code stable** et validé.

. Branche dev
- C’est la branche de **développement central**.
- Toutes les fonctionnalités testées sont fusionnées ici avant d’aller dans `main`.

 Branche feature

- Ce sont les branches utilisées pour **développer individuellement** chaque fonctionnalité.
- Dans ton projet, on aura :
  - `feature/html-structure`
  - `feature/css-theme`
  - `feature/js-interactions`


. Branche test/frontend
- C’est la branche utilisée pour les **tests d’intégration**.
- On y fusionne les branches `feature/*` pour :
  - Vérifier la cohérence visuelle
  - Tester les animations, carrousels, menu responsive, etc.
  - S’assurer que tout fonctionne bien ensemble

. Fusion vers `dev`, puis `main`
- Une fois les tests validés :
  - `test/frontend` est fusionnée dans `dev`
  - Puis `dev` est fusionnée dans `main`



Résumé graphique


main
 └─ dev
      ├─ feature/html-structure
      ├─ feature/css-theme
      └─ feature/js-interactions
             ↓
        test/frontend
             ↓
           dev
             ↓
