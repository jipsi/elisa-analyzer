# ELISA Analyzer

Interactive single-page tool for ELISA standard curve fitting and 96-well plate simulation. No install needed — just open in a browser.

**[Live Demo →](https://jipsi.github.io/elisa-analyzer/elisa_analyzer.html)**

## What it does

- **Standard curve fitting** — 4-Parameter Logistic (4PL) and Linear models with interactive parameter sliders
- **96-well plate simulation** — colour-coded dot plot with configurable serial dilution, duplicate/triplicate standards, and sample conditions
- **Back-calculation** — imputes unknown sample concentrations from the fitted curve, with automatic >ULoQ / <LLoQ flagging
- **Error simulation** — pipette errors, air bubbles, edge effects, cross-contamination, and incomplete washes to see how common lab artefacts affect results

## Usage

Open [`elisa_analyzer.html`](elisa_analyzer.html) in any modern browser. The only dependency is Plotly.js (loaded from CDN).

- Change **serial dilution** or **start concentration** to see how standard spacing affects curve fit quality
- Click **Regenerate Plate** for fresh stochastic noise
- Use the **Simulate** buttons above the plate to introduce realistic errors
- Switch between **4PL** and **Linear** models; adjust 4PL parameters with sliders

## Tech

Single HTML file — vanilla JS, CSS, and [Plotly.js](https://plotly.com/javascript/). 4PL fitting via Nelder-Mead optimisation.
