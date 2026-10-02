# Vector Database with HNSW Indexing

A hierarchical graph ANN index implemented from scratch with exact-search comparison, tombstones and checksummed persistence.

This is newly generated educational reference code based on a concept in the supplied PDF.
It has **165 non-empty source, test, configuration, workload and documentation files**.
It is a prototype for study and extension, not evidence of previous deployment or measured large-scale performance.

## Quick start

Requires Python 3.10+; the default path uses the standard library.

```sh
python scripts/demo.py
python scripts/run_tests.py
python scripts/benchmark.py
python scripts/serve.py --port 8080
```

Open http://127.0.0.1:8080 for the workload dashboard. `scripts/demo.py --case workloads/<id>.case.json`
executes one workload and checks its independent acceptance conditions. `benchmark.py` prints actual local timings.

## Implemented scope

Random level assignment, greedy upper-layer navigation, ef-limited priority-queue search, neighbor diversification/pruning, insertion, deletion filtering, exact L2 baseline, persistence and an operation service class.

## Limits and optional runtimes

Python reference, not a million-vector production database. No embedding model, concurrency control, compressed vectors or live gRPC transport. proto schema is a design artifact only. Graph links may become asymmetric after per-node degree pruning. Deleted nodes remain in memory; rebuilding is needed for reclamation. Checksums are not authenticity signatures.

All bundled data are synthetic. No credentials, pretrained model weights, historical commits, or fabricated benchmark results are included.
See `docs/PROVENANCE.md`, `docs/TESTING.md`, and the bundle's validation report for evidence and omissions.
