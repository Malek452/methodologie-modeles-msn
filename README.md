# MSN · Linear and exponential models

A standalone French teaching presentation for **TD1, exercises 2 and 5**, based on the supplied `TD1-MSN-corrige-complet.tex`. It teaches how to choose a model, identify its parameters, build formulas and justify each calculation.

[Live presentation](https://malek452.github.io/methodologie-modeles-msn/) · [Printable handout](https://malek452.github.io/methodologie-modeles-msn/handout/) · [Version française](README.fr.md)

## Course

- [General method](https://malek452.github.io/methodologie-modeles-msn/#activity/choisir-modele): additive versus multiplicative change, units, assumptions, parameters and threshold equations.
- [Exercise 2](https://malek452.github.io/methodologie-modeles-msn/#activity/ex2-reperes): cumulative production with an unknown constant rate, a pause and a piecewise affine model.
- [Exercise 5](https://malek452.github.io/methodologie-modeles-msn/#activity/ex5-modele): continuous exponential growth, populations after 15 h and 20 h, and the time needed to reach 50,000 bacteria.

Each step pairs a formula or graph with its justification. The lesson explicitly distinguishes supplied data from modelling assumptions. The handout includes the complete reasoning and graphs.

## Independent project

This repository was created from the [Atelier Présentations template](https://github.com/Malek452/atelier-presentations). The template is the source of the presentation engine, not this course's deployment destination. Make changes and publish this course only from `Malek452/methodologie-modeles-msn`; keep the upstream template independent.

The inherited recipes in `examples/` remain available as authoring references and independent regression fixtures. They are not part of the active course.

## Run locally

Install Node.js 24, then work in this repository:

```sh
npm ci
npm run dev
```

The first launch compiles the equations and animation player. After editing lesson content, wait for recompilation and reload the page. The production output is `dist/`.

## Edit the presentation

| File | Purpose |
| --- | --- |
| `src/content/methodologie-modeles.ts` | General method |
| `src/content/production-lineaire.ts` | Exercise 2 |
| `src/content/croissance-exponentielle.ts` | Exercise 5 |
| `src/content/index.ts` | Registered sections and their order |
| `presentation.config.ts` | Title, description and interface language |
| `src/theme.ts` | Shared presentation palette |

Read [AGENTS.md](AGENTS.md), the [authoring guide](docs/AUTHORING.md) and [animation recipes](docs/ANIMATIONS.md) before changing the content. Keep activity IDs stable so existing links continue to work.

## Reader controls

Choose a chapter and activity, then use the buttons, **← / →** or a horizontal swipe to move through the explanation. The step selector allows direct jumps. Playback, pause, replay, speed, reduced motion and fullscreen controls are included. **Space** toggles playback when focus is outside a control.

Backward navigation shows the completed step. Replay restores the authored forward transition. No accounts, answers or student progress are collected; only the reduced-motion preference is stored locally.

## Validate and publish

```sh
npm run validate  # tests, typecheck and production build
npm run preview   # inspect dist/ locally
```

The **Deploy to GitHub Pages** workflow validates and publishes pushes to `main` in this repository. It also supports manual dispatch. Configure **Settings → Pages → GitHub Actions** for this independent repository. Deployment publishes only `dist/`, including the handout and animation assets, to the presentation's own URL.

The tests check authored formulas, production joins, population values, logarithmic equations, navigation and rendering. They supplement mathematical and visual review. See [deployment](docs/DEPLOYMENT.md), [architecture](docs/ARCHITECTURE.md) and [maintenance](docs/MAINTENANCE.md) for technical details.

## Attribution and license

The presentation engine comes from [Atelier Présentations](https://github.com/Malek452/atelier-presentations), under the MIT license. Keep [LICENSE](LICENSE) and [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md). The teaching content is adapted from the supplied TD1 correction; rights to separately added materials remain their respective owners'.
