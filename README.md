# emulsion-tracker
Measuring and modelling emulsion destabilisation from creaming index time-series

This self-directed project is a home study tracking creaming in 14 oil-in-water emulsions over 259 hours, comparing a thickener series against an emulsifier series.

Key result:

<img width="452" height="178" alt="image" src="https://github.com/user-attachments/assets/3e7fdc5d-bec8-4ec3-8442-a1fce1cff466" />

Polysorbate 80 reduced the creaming rate constant monotonically (0.0678 → 0.0030 h⁻¹), saturating above 1%.

Xanthan was non-monotonic: 0.05% increased it by ~27% before higher concentrations cut it by almost 30x  — consistent with depletion flocculation competing with the viscosity rise.

Both converged on ~0.003 h⁻¹ at their top concentrations by different mechanisms, so creaming rate alone can't distinguish the two routes to stability.

Method summary:
14 cylinders of 20% o/w sesame oil emulsion, seven formulations in duplicate: control, xanthan (0.05/0.10/0.20%) and polysorbate 80 (0.5/1.0/2.0%). Creaming index read off the graduations over 259 h, with CI(t) = CI_max(1 − e^(−kt)) fitted per cylinder via scipy.optimize.curve_fit. One cylinder excluded (disturbed); run ended when microbial growth appeared.
