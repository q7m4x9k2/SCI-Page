# Self-Governed Collective Intelligence

Anonymous project page for **Self-Governed Collective Intelligence (SCI)**, with the paper summary, result figure, and 45 interactive case studies: the original 40 examples plus five additional cases in medical image understanding and geometric reasoning.

## Build and preview

Requires Node.js 24 or later.

```sh
npm ci
npm run dev
```

To validate and build the static site:

```sh
npm run build
```

The generated site is written to `dist/`. The included GitHub Actions workflow builds and deploys the site with GitHub Pages when changes are pushed to `main`.

## Content

- `src/paper.mdx`: project summary and result figure.
- `src/data/caseSamples.json`: case gallery index.
- `public/cases/case_pages/`: individual case visualizations.
- `public/cases/assets/`: images used by the case visualizations.

The case pages and all referenced assets are included. Building the website does not require the original experiment directories. The historical `scripts/sample-cases.mjs` utility rebuilds a different selection from upstream analysis outputs; it is not part of this 45-case release build and must not be used to overwrite the combined gallery.

## Template credits and license

The website uses [Roman Hauksson's Academic Project Astro Template](https://github.com/RomanHauksson/academic-project-astro-template). That template was adapted from [Eliahu Horwitz's Academic Project Page Template](https://github.com/eliahuhorwitz/Academic-project-page-template), which was adapted from [Keunhong Park's Nerfies project page](https://nerfies.github.io/).

The original website template is licensed under the [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/). This attribution is retained for the adapted website template. The paper content and third-party case images are separate from the template attribution.


## Case interpretation

The gallery retains the original 40 examples and adds five selected medical and geometric reasoning examples. These 45 case records are selected illustrations, not an estimate of dataset accuracy. The chest-radiograph case has no recorded standalone baseline; its comparison starts at iteration 1. The cube-transformation case shows the saved gallery aggregation, with its earlier raw final answer disclosed on the page. Two medical cases contain structured support and votes without the full reasoning narrative in their saved exports.

Medical depth visualizations were generated separately with Depth Anything V2 Large after the original experiments. They are labeled supplemental wherever displayed and were not used in the recorded iterations. These are relative model outputs, not metric anatomical distances.
