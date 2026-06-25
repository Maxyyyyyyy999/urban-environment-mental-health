# Urban Environment & Mental Health · UK Biobank

An interactive single-page website exploring whether the urban environment shapes
mental health, using data from the **UK Biobank** cohort. It walks through the full
research pipeline — from question and background to data, methods, and results — with
interactive, in-browser visualizations.

## Live site

If GitHub Pages is enabled, the site is served at:
`https://maxyyyyyyy999.github.io/urban-environment-mental-health/`

## What's inside

The page covers:

- **Research question** — does the urban environment shape mental health, and through what pathways?
- **Background** — UK Biobank, Places365 scene recognition, and environmental epidemiology.
- **Data** — cohort construction (502,128 → 156,438 → 135,541), variables, and missingness.
- **Methods & Results** — OLS + SHAP, WQS mixtures, dose–response curves, and mediation analysis.
- **Imagery → environment** — planned street-view feature extraction feeding the mixture/mediation models.

### Interactive features (run entirely in your browser)

- Distribution + Box–Cox power-transform explorer (drag a slider, watch skewness move).
- Correlation matrix with hover values.
- Predictor-vs-depression relationship explorer.
- "Build your own regression" — an OLS model that refits live on a real-data sample.
- Residual / Q-Q diagnostics and a live prediction profiler.

## Structure

```
.
├── index.html      # the entire site (markup, styles, and interactive logic)
├── data.js         # dataset for the interactive visualizations
├── regdata.js      # sample data for the live regression
└── assets/         # result figures
    ├── shap.png
    ├── wqs.png
    ├── doseresponse.png
    └── mediation.png
```

## Running locally

It's a static site — just open `index.html` in a browser, or serve the folder:

```bash
python -m http.server 8000
# then visit http://localhost:8000
```

## Notes

This is a research / data-communication project. Parts of the analysis (notably the
street-view imagery features) are marked as work in progress on the site itself.
