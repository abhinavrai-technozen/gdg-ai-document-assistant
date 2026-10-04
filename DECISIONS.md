# Configuration Experiments & Decisions

## Experiment 1 (Large Chunks)
- **Chunk Size:** 1000 characters
- **Chunk Overlap:** 100 characters
- **Retriever Top-K:** 2
- **Observation:** Broader context retrieved, but lower precision on specific sentence boundaries and page attribution.

## Experiment 2 (Optimal Small Chunks - Selected)
- **Chunk Size:** 500 characters
- **Chunk Overlap:** 50 characters
- **Retriever Top-K:** 3
- **Observation:** Significantly better grounding accuracy, clearer passage extraction, and exact source page tracking.
