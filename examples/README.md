# R0 JSON configuration

Use the maintained
[spires-batch R0 template](https://github.com/RittgerLabGroup/spires-batch/blob/main/examples/r0.json)
and its [walkthrough](https://github.com/RittgerLabGroup/spires-batch/blob/main/examples/r0.md).
The complete five-tile sequence uses `workflow.json` and `workflow.md` in the same
examples directory. These configurations are consumed by the batch planner,
which calls this package's public R0 API; spires-r0 is not a JSON submission CLI.

Choose the intended processing WY and the previous-summer recipe, or provide
explicit dates when needed.
All summer scenes for one tile/year must fit in RAM before selection. Request a
full-memory exclusive blanca-snow node for full tiles. Products are atomic NetCDF;
Zarr staging and chunked R0 execution are not supported. Valid existing R0 assets
can be reused rather than regenerated on each historical or NRT run.
