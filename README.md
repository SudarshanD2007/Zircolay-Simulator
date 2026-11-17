# Zircaloy Steam-Oxidation Lab (GitHub Pages)

A static browser-based educational simulator. It requires no Python, server, package installation, or build step.

## Publish with GitHub Pages

1. Create a new GitHub repository (for example `zircaloy-oxidation-lab`).
2. Upload `index.html` to the repository root.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Select branch `main` and folder `/ (root)`, then Save.
6. Wait for the deployment and open the URL GitHub Pages provides.

The site is entirely client-side. All calculations run in the visitor's browser. No data is sent to a server.

## What's inside

- Arrhenius temperature dependence for an effective oxygen diffusivity.
- 1D transient Fickian diffusion, solved with an explicit finite-difference scheme.
- A separate illustrative parabolic oxide-growth law.
- Stoichiometric estimates of hydrogen production and oxidation heat from estimated zirconium consumption.
- Concentration and oxide-growth plots.
- A simple investigation notebook and CSV/JSON exports.

## Important scientific limitations

This is an educational prototype, not a validated reactor accident code.

- The diffusion calculation is a single-region teaching model. It does not resolve separate ZrO2 / alpha-Zr(O) / substrate domains or their moving interfaces.
- The oxide-growth law is an illustrative, user-calibrated parabolic law. The default values are NOT Cathcart-Pawel coefficients. Replace them with traceable coefficients from the exact primary source and alloy/temperature range before quantitative use.
- Steam pressure enters through a simplified multiplier, not a detailed gas-film or chemical-potential boundary condition.
- The layer illustration is schematic and not a computed phase-boundary location.
- The model does not calculate fuel temperature, cladding rupture, fission power, decay heat, core damage, meltdown, radiation release, or hydrogen combustion.
- The hydrogen and reaction-heat estimates use planar unit-area assumptions and reaction stoichiometry. They are not accident consequence predictions.

## Suggested next research upgrades

1. Implement a coupled multilayer moving-boundary solver with partitioning and interface mass balances.
2. Replace illustrative kinetics with verified Cathcart-Pawel equations and a clearly documented validity window.
3. Add temperature-dependent material properties and an independently validated heat-transfer model only if the project scope supports it.
4. Add benchmark comparisons, mesh/time-step convergence tests, and oxygen mass-balance closure.

## Local preview

Open `index.html` directly in a modern browser. No local server is required.
