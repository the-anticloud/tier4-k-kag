# Developer Cookbook — K_KAG
**Stack:** Python 3.11, KANTOR_K5, spaCy 3.7+, PAX 27B, AIOSS_FORMAT
**Domain:** Knowledge-Augmented Generation: structured fact injection into PAX 27B inference

## Knowledge-augmented generation
```python
from k_kag import KAGPipeline

kag = KAGPipeline(
    pax_model="./pax-27b-q4.gguf",
    kantor_db="./kantor_k5.db",
    aioss_chain="./kag.aioss"
)

result = kag.generate(
    query="What is the TRL level and HIPAA compliance status of K_BRAINFLOW?",
    max_tokens=256
)
print(result.answer)
print(f"Injected {len(result.injected_facts)} facts, accuracy score: {result.accuracy_score:.2f}")
print(f"Chain: {result.chain_hash}")
```

## Inspect injected facts
```python
for fact in result.injected_facts:
    print(f"  [{fact.predicate}] {fact.subject}: {fact.value}")
# [trl_level] K_BRAINFLOW: TRL-8
# [regulatory] K_BRAINFLOW: HIPAA Safe Harbor compliant
```

## Freshness check
```python
kag.check_fact_freshness("K_BRAINFLOW TRL", max_age_days=30)
```

## Benchmark KAG vs baseline
```python
bench = kag.benchmark("./factual_bench.jsonl")
print(f"KAG accuracy: {bench.kag:.2f} | Baseline: {bench.baseline:.2f}")
print(f"Hallucination: KAG={bench.kag_hallucination:.2%} Base={bench.base_hallucination:.2%}")
```

## AIOSS Chain Append
```python
import hashlib, time

def aioss_append(chain_path, payload: bytes, module_id: str):
    entry_hash = hashlib.sha3_256(payload).digest()
    ts = int(time.time_ns()).to_bytes(8, 'big')
    with open(chain_path, 'rb') as f:
        f.seek(-32, 2); prev_hash = f.read(32)
    new_hash = hashlib.sha3_256(prev_hash + entry_hash + ts).digest()
    with open(chain_path, 'ab') as f:
        f.write(ts + entry_hash + new_hash)
    return new_hash.hex()
```
