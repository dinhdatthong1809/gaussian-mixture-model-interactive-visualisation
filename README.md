# Gaussian Mixture Model — Interactive Visualisation

A dependency-free browser demo of how a Gaussian Mixture Model is fitted with
the EM algorithm. Click to add data, then step through the algorithm and watch
the model converge.

**Live demo:** https://dinhdatthong1809.github.io/gaussian-mixture-model-visualization/

## Features

- **1D or 2D data** — add points by clicking, or load a sample dataset.
- **Two ways to draw the model** — sigma ellipses (1σ / 2σ / 3σ) or a
  pseudo-3D "mountain" density surface.
- **Step-by-step EM** — run the E step and the M step separately, one
  iteration, ten iterations, or auto-run until convergence.
- **Soft assignment made visible** — every dot is coloured by blending the
  cluster colours with its membership probabilities, so points in the overlap
  show an in-between colour.
- **English / Vietnamese** interface (English by default).

## Running locally

No build step and no dependencies — just open the page:

```bash
git clone https://github.com/dinhdatthong1809/gaussian-mixture-model-visualization.git
cd gaussian-mixture-model-visualization
open index.html            # macOS; Linux: xdg-open index.html
```

Or serve it over HTTP:

```bash
python3 -m http.server 8000   # then open http://localhost:8000/
```

## Files

| File | Purpose |
| --- | --- |
| `index.html` | Page structure and controls |
| `style.css` | Styling |
| `app.js` | EM algorithm, canvas rendering and the translation table |

The sample 1D dataset is the "energy score" of 20 songs, taken from the
companion repository
[gaussian-mixture-model](https://github.com/dinhdatthong1809/gaussian-mixture-model),
which fits the same model with scikit-learn.
