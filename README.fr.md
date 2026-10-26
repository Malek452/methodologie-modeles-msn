# MSN · Modèles linéaires et exponentiels

Une présentation pédagogique autonome pour les **exercices 2 et 5 du TD1**, construite à partir du corrigé fourni `TD1-MSN-corrige-complet.tex`. Elle explique comment choisir un modèle, identifier ses paramètres, construire une formule et justifier chaque calcul.

[Présentation en ligne](https://malek452.github.io/methodologie-modeles-msn/) · [Support imprimable](https://malek452.github.io/methodologie-modeles-msn/handout/) · [English](README.md)

## Parcours

- [Méthode générale](https://malek452.github.io/methodologie-modeles-msn/#activity/choisir-modele) : distinguer évolution additive et multiplicative, définir les unités, annoncer les hypothèses et résoudre une question de quantité ou de date.
- [Exercice 2](https://malek452.github.io/methodologie-modeles-msn/#activity/ex2-reperes) : cadence inconnue `r`, production cumulée, pause, fonction affine par morceaux et total `9r` à 18 h.
- [Exercice 5](https://malek452.github.io/methodologie-modeles-msn/#activity/ex5-modele) : `N(t) = 100 × 3^(t/3)`, effectifs après 15 h et 20 h, seuil de 50 000 bactéries et limites du modèle continu.

Chaque étape associe une formule ou un graphique à sa justification. Les données de l’énoncé sont distinguées des hypothèses de modélisation. Le support imprimable rassemble les raisonnements et les graphiques.

## Un projet indépendant

Ce dépôt a été créé à partir du [modèle Atelier Présentations](https://github.com/Malek452/atelier-presentations). L’atelier fournit le moteur ; il reste indépendant de cette présentation. Toute modification et toute publication de ce cours doivent se faire dans `Malek452/methodologie-modeles-msn`, avec sa propre adresse.

Les recettes héritées dans `examples/` restent des références de rédaction et des jeux de tests indépendants. Elles ne sont pas inscrites dans le parcours actif.

## Exécuter localement

Installer Node.js 24, puis exécuter dans ce dépôt :

```sh
npm ci
npm run dev
```

Le premier lancement compile les formules et les animations. Après modification du contenu, attendre la recompilation puis recharger la page. La version destinée à la publication est produite dans `dist/`.

## Modifier le cours

| Fichier | Rôle |
| --- | --- |
| `src/content/methodologie-modeles.ts` | Méthode générale |
| `src/content/production-lineaire.ts` | Exercice 2 |
| `src/content/croissance-exponentielle.ts` | Exercice 5 |
| `src/content/index.ts` | Chapitres inscrits et ordre du parcours |
| `presentation.config.ts` | Titre, description et langue des commandes |
| `src/theme.ts` | Palette commune de la présentation |

Lire [AGENTS.md](AGENTS.md), le [guide de rédaction](docs/AUTHORING.md) et les [recettes d’animation](docs/ANIMATIONS.md) avant de modifier le contenu. Conserver les identifiants des activités pour préserver les liens existants.

## Navigation

Choisir un chapitre et une activité, puis avancer avec les boutons, les flèches du clavier ou un glissement horizontal. Le sélecteur d’étape permet un accès direct. La lecture automatique, la pause, le ralenti, le rejeu, le plein écran et la réduction des animations sont disponibles.

Un retour en arrière montre l’étape terminée ; le rejeu restitue la transformation dans son sens initial. Aucun compte, résultat ou suivi d’étudiant n’est collecté. Seule la préférence de réduction des animations est conservée localement.

## Vérifier et publier

```sh
npm run validate
npm run preview
```

Le workflow **Deploy to GitHub Pages** valide et publie les pushes sur `main` dans ce dépôt. Il peut également être lancé manuellement. La source de publication de ce projet indépendant doit être **Settings → Pages → GitHub Actions**. Seul `dist/`, avec le support imprimable et les animations, est déployé à l’adresse propre du cours.

Les tests vérifient les formules rédigées, les raccords de production, les effectifs, les équations du seuil, la navigation et le rendu. Ils complètent la revue mathématique et visuelle. Voir les guides de [publication](docs/DEPLOYMENT.md), d’[architecture](docs/ARCHITECTURE.md) et de [maintenance](docs/MAINTENANCE.md).

## Attribution et licence

Le moteur provient d’[Atelier Présentations](https://github.com/Malek452/atelier-presentations), sous licence MIT. Conserver [LICENSE](LICENSE) et [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md). Le contenu pédagogique est adapté du corrigé TD1 fourni ; les droits sur les documents ajoutés séparément restent ceux de leurs titulaires.
