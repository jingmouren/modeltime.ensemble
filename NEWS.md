# modeltime.ensemble (development version)

- Move `modeltime_fit_resamples()` to a new package `modeltime.resample`.

# modeltime.ensemble 0.2.0

__Stacked Ensembles (Breaking Changes)__

The process for creating stacked ensembles is split into 2 steps:

- Step 1: Use `modeltime_fit_resamples()` to generate resampled predictions
- Step 2: Use `ensemble_model_spec()` to apply stacking using a `model_spec`

Note - `modeltime_refit(stacked_ensemble)` is still one step, which is the best way to handle refitting since multiple stacked models may have different submodel compositions. An additional argument, `resamples` can be provided to train stacked ensembles made with `ensemble_model_spec()`.

# modeltime.ensemble 0.1.0

* Initial release of `modeltime.ensemble`.
