# Generative-AI decision-support experiments

Small, auditable experiments for structured decision support. The default workflow is deterministic, requires no API key, and demonstrates input validation, provenance, and human-review boundaries. The original API experiment is preserved under `src/legacy/`.

## Quick start

```bash
python workflow.py --input examples/input.csv --config config/workflow.json --output output
python -m unittest discover -s tests -v
```

If adapting the legacy API example, load credentials from the environment, pin the model and SDK version, avoid sending confidential data, and record prompts/responses according to applicable policy. Generated recommendations require human review and must not directly trigger high-impact actions.
