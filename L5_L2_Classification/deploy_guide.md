# Deploy Guide — K_KAG
**Tier:** TIER_4_INFERENCE_AGENTS | **Stack:** Python 3.11, KANTOR_K5, spaCy 3.7+, PAX 27B, AIOSS_FORMAT
**Air-gap capable after initial setup.**

## Prerequisites
Python 3.11+, KANTOR_K5 database (populated), spaCy 3.7+, PAX 27B weights.

## Environment
8GB RAM. GPU for PAX generation. KANTOR_K5 must be populated with project facts.

## AIOSS Integration
```bash
aioss init --module K_KAG --output ./k_kag.aioss
aioss append --chain ./k_kag.aioss --payload ./output.bin --module K_KAG
aioss verify --chain ./k_kag.aioss
```

## Air-Gap Setup
```bash
pip download -r requirements.txt -d ./wheels/
pip install --no-index --find-links ./wheels/ -r requirements.txt
```

## PAX 27B Harness Wiring
```python
from anticloud_pax import PAXHarness
harness = PAXHarness(
    model_path="./pax-27b-q4.gguf",
    module="K_KAG",
    aioss_chain="./K_KAG.aioss",
    classification="L5_NARROW_L2_GENERAL"
)
result = harness.process(input_data)
```

## Verification
```bash
aioss verify --chain ./K_KAG.aioss --verbose
python -m K_KAG.tests.smoke
```
