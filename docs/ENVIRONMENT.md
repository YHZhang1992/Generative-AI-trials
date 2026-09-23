# Environment: AI decision-support prototype

## Standard profile

The canonical `workflow.py` portable profile uses Python 3.10+ and the standard library only, so its example and smoke test run without package installation. It establishes input validation, deterministic processing, output structure, figures, and provenance. Use the advanced implementation for production-grade domain methods.

Do not install the union of every historical dependency. Select the advanced canonical entry point, separate standard-library/local imports from external packages, and create a per-workflow lockfile.

Detected imports (static, may include local modules or command tokens):

`openai, os`

- Python: declare dependencies and interpreter range in `pyproject.toml`; create and commit `uv.lock`.
- R: initialize `renv`, install approved CRAN/Bioconductor versions, then commit `renv.lock`.
- Hybrid/bioinformatics: use the supplied Conda manifest where available and record STAR, samtools, Cell Ranger, reference genome, annotation, and gene-set versions.

## Controlled/GxP profile

No constrained-package implementation is supplied for this topic.

Never install or update packages inside an analysis run. Qualification must pin exact versions on the target platform and retain installation evidence.
